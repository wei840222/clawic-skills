# Store Specifications and Pre-Upload Checks

## Authoritative sources

Store requirements change independently of this skill. Before creating final exports, verify the selected platform's current requirements:

- Apple — [Screenshot specifications](https://developer.apple.com/help/app-store-connect/reference/screenshot-specifications)
- Google Play — [Add preview assets to showcase your app](https://support.google.com/googleplay/android-developer/answer/9866151)

Record the source page date (if shown), selected device classes, locales, and required asset count in `<state_root>/{app-slug}/config.md`. Do not infer a current upload requirement from an old project folder.

## Apple App Store

1. In App Store Connect, select the app version, device family, and localizations to be delivered.
2. Use the current Apple table for the required screenshot pixel dimensions and accepted file rules for each selected device family.
3. Export one consistent set per localization. Keep essential copy away from rounded corners, status-bar areas, and any crop-prone edges.
4. Before upload, confirm the files match the current Apple dimensions, format, color-space, transparency, count, and file-size rules.

If a source capture cannot be reframed without obscuring product UI or copy, return to the composition step and create a target-specific layout instead of stretching the image.

## Google Play

1. In Play Console, select the app and the device types that will receive screenshots.
2. Verify the current Google Play requirements for phone/tablet screenshots and feature graphics when applicable.
3. Export only supported image formats and dimensions, with readable copy at the store listing scale.
4. Before upload, inspect each localization and device class in the Play Console preview.

If Play Console rejects an asset, retain the validation message, correct only the reported constraint, then rerun the full pre-upload checklist for that asset set.

## Composition safeguards

- Build from the highest-resolution raw capture available.
- Keep a single visual message per screenshot and adapt copy placement to each target aspect ratio.
- Prefer reframing or a platform-specific composition over cropping critical product content.
- Inspect previews at thumbnail scale and at full resolution; correct unreadable text, unsafe margins, inconsistent frames, and visible sensitive data before delivery.
