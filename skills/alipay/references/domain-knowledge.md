# Alipay Domain Knowledge

This reference provides essential domain context and constraints for integrating Alipay globally. Prefer official Alipay documentation when endpoint, signing, sandbox, or notification behavior is time-sensitive.

## Mobile vs Web
- **Alipay App Integration (App Pay)**: Uses an SDK (iOS/Android) where the merchant's server signs the order, the app sends it to the Alipay SDK, and the SDK opens the Alipay app.
- **WAP / Mobile Web**: Redirects the user's mobile browser to Alipay's secure H5 checkout.
- **PC Web**: Redirects to a desktop checkout page where the user can scan a QR code using their Alipay app.

## Cross-Border Payments
Alipay Global supports cross-border transactions where merchants receive funds in their local currency while the customer pays in RMB. Currency conversion is handled automatically by Alipay's daily exchange rate.

## Sandbox Environment
When testing, always use the Alipay Sandbox (`https://openapi-sandbox.dl.alipaydev.com/gateway.do`) and a dedicated sandbox merchant app ID. Production and Sandbox keys must strictly be isolated.

## Idempotency and Async Notifications
Alipay heavily relies on asynchronous notifications (callbacks) to confirm payment success. Your webhook endpoint must:
- Verify the RSA/RSA2 signature.
- Verify the `app_id` matches your app.
- Verify the `out_trade_no` and `total_amount`.
- Respond exactly with the string `success` to stop Alipay from retrying the notification.

## Official Sources
- **Alipay Open Platform documentation** — product and API entry via https://opendocs.alipay.com/
- **Alipay Global / Cross-border developer docs** — wallet and overseas merchant guidance via https://global.alipay.com/docs/
- **Production gateway** — `https://openapi.alipay.com/gateway.do`
- **Sandbox gateway** — `https://openapi-sandbox.dl.alipaydev.com/gateway.do`
