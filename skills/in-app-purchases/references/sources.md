# Research Sources — in-app-purchases

Full URLs used for Gate 6 knowledge updates. Prefer these over model memory for unstable pricing, policy, or API claims.

## Apple StoreKit / App Store Server

- **StoreKit** — product request, purchase, Transaction, finish, and StoreKit 2 overview via https://developer.apple.com/documentation/storekit
- **In-App Purchase** — product types, restore, and App Store IAP concepts via https://developer.apple.com/in-app-purchase/
- **App Store Server API** — server-side transaction lookup and signed renewal info via https://developer.apple.com/documentation/appstoreserverapi
- **App Store Server Notifications V2** — subscription lifecycle webhook events via https://developer.apple.com/documentation/appstoreservernotifications
- **Original API for In-App Purchase** (legacy verifyReceipt context) via https://developer.apple.com/documentation/in-app-purchase

## Google Play Billing

- **Google Play Billing Library overview** via https://developer.android.com/google/play/billing
- **Billing library integration** via https://developer.android.com/google/play/billing/integrate
- **Real-time developer notifications** via https://developer.android.com/google/play/billing/rtdn-reference
- **Purchase verification / Play Developer API** via https://developers.google.com/android-publisher

## RevenueCat and managed layers

- **RevenueCat docs home** via https://www.revenuecat.com/docs
- **RevenueCat webhooks** via https://www.revenuecat.com/docs/webhooks
- **RevenueCat pricing / MTR framing** via https://www.revenuecat.com/pricing/
- **Offerings and entitlements model** via https://www.revenuecat.com/docs/entitlements

## Policy and paywall compliance

- **App Store Review Guidelines** (IAP, subscriptions, external links) via https://developer.apple.com/app-store/review/guidelines/
- **Google Play Payments policy** via https://support.google.com/googleplay/android-developer/answer/9858738
- **Apple Subscriptions guide** via https://developer.apple.com/app-store/subscriptions/

## Analytics baselines

- Use vendor dashboards plus `references/analytics.md` for trial conversion, renewal, refund, and grace-period instrumentation.
- Prefer first-party store or RevenueCat charts over stale third-party “industry average” screenshots unless the source URL is current.

## Notes

- MTR free tiers and percentage fees change; re-check vendor pricing pages before quoting commercial terms.
- Sandbox renewal compression tables change; re-check Apple’s current sandbox testing documentation before timing automated tests.
