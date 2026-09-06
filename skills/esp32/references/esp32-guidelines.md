# ESP32 engineering guidelines

Apply these rules after identifying the exact chip, board schematic, framework, and version. The original ESP32 pin map and APIs differ from later ESP32-family variants.

## GPIO and analog input

- Check the board schematic and the chip's GPIO matrix before assigning a pin. Boot-strapping pins, flash/PSRAM connections, input-only GPIOs, and board peripherals constrain usable pins.
- On the original ESP32, GPIO6–GPIO11 are commonly connected to SPI flash; reserve them for flash unless the board documentation explicitly says otherwise.
- On the original ESP32, GPIO34–GPIO39 are input-only and lack internal pull-up/pull-down resistors.
- With original-ESP32 Wi-Fi active, route analog reads to an ADC1-capable pin. ADC2 access is shared with Wi-Fi and is not a dependable concurrent design.
- For a pin-level decision, load the target's GPIO and ADC documentation and confirm the board's net assignment.

## Deep sleep and wakeup

- Select wake sources that the target chip and board expose in deep sleep; RTC-capable GPIO availability varies by chip.
- Persist only intentionally retained values with the framework's RTC-memory mechanism; ordinary RAM is not a deep-sleep persistence mechanism.
- For a single external wake signal, use the target framework's single-pin external-wakeup API. For multiple signals, use its supported multi-pin external-wakeup mode and validate the required logic level and pull resistors.
- Treat reconnect latency after wake as part of the product flow. Measure it on the deployed network rather than relying on a fixed delay estimate.
- If wakeup fails, first verify chip support, RTC-capable pin selection, wake polarity, and external pull configuration against the board schematic.

## Wi-Fi

- Set the intended Wi-Fi mode before starting a connection, then use framework events for connection and IP-state changes.
- Implement reconnect policy with bounded retry and backoff appropriate to the device's power budget; verify it under AP loss and recovery.
- Evaluate static addressing only when the network has a managed reservation/addressing plan. DHCP behavior and connection time vary with the network.

## FreeRTOS and watchdogs

- Size each task stack from measured high-water-mark data on the target build; network, logging, and formatting paths can require more stack than simple loops.
- Ensure every long-running task yields, blocks, or otherwise cooperates with scheduling. Configure and service watchdogs according to the framework version and task role.
- Use core affinity only when the target/framework supports it and a measured contention or timing requirement justifies it.
- If a watchdog triggers, capture the backtrace and task state, then inspect blocking loops, stack pressure, and scheduling before extending timeouts.

## Memory

- Monitor free heap, minimum free heap, and the appropriate capability-specific heap where supported. Preallocate long-lived buffers and avoid churn in constrained heaps.
- Verify PSRAM availability from the board configuration and allocate through the framework's documented capability-aware API when it is suitable.
- Prefer bounded buffers or pre-reserved strings for repeated construction of dynamic text.

## Peripherals

- Configure PWM through the framework's LEDC/PWM APIs; do not assume Arduino-like analog-write behavior is portable across frameworks or chip variants.
- Confirm I2C pull-up resistance, bus voltage, speed, and board routing. Internal pull-ups rarely replace an electrical design for a fast or long bus.
- Configure SPI chip select explicitly when the device/driver requires it.
- Reserve the console/USB UART used by flashing and diagnostics; choose an available UART and pins for external devices.

## OTA and power

- Confirm a dual-OTA partition layout, image size headroom, rollback policy, and a recovery path before enabling field OTA.
- Keep OTA handling responsive to the framework's requirements and isolate it from timing-critical work.
- Design the supply for measured transmit-current peaks with suitable decoupling. Validate brownout behavior on the actual battery, cable, and radio workload.
- Measure deep-sleep current on the assembled board; enabled RTC domains, regulators, sensors, and pull networks affect total current.

## Primary sources

Use the documentation matching the target chip and framework release:

- ESP-IDF GPIO — https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-reference/peripherals/gpio.html
- ESP-IDF sleep modes — https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-reference/system/sleep_modes.html
- ESP-IDF heap memory allocation — https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-reference/system/mem_alloc.html
- ESP-IDF FreeRTOS — https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-reference/system/freertos_idf.html
- ESP-IDF Wi-Fi — https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-reference/network/esp_wifi.html
