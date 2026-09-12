# Sources — Shelly

Use these official sources when Shelly Gen2+ RPC methods, authentication, component behavior, or cloud product guidance matter.

## Gen2+ API and RPC

- Shelly API docs home: https://shelly-api-docs.shelly.cloud/
- Shelly Gen2 devices documentation: https://shelly-api-docs.shelly.cloud/gen2/
- RPC protocol overview: https://shelly-api-docs.shelly.cloud/gen2/General/RPCProtocol/
- Authentication: https://shelly-api-docs.shelly.cloud/gen2/General/Authentication/
- Switch component (common relay control): https://shelly-api-docs.shelly.cloud/gen2/ComponentsAndServices/Switch/

## Product and Support Context

- Shelly Knowledge Base: https://kb.shelly.cloud/knowledge-base
- Shelly support landing: https://www.shelly.com/en-us/pages/support

## Usage Notes

- Prefer `shelly-api-docs.shelly.cloud` over third-party blogs for method names, params, and auth requirements.
- Gen1 and Gen2 method surfaces differ; confirm the device generation before choosing RPC methods.
- Cloud token scope and account permissions change by product and region; verify live account settings before fleet writes.
- Treat MQTT topic layouts as deployment-specific; confirm broker ACLs and retained-message policy before automation.
