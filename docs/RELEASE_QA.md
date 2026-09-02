# Verseborne 1.0 release QA

This is a public summary of the release-candidate checks. Signed binaries, provisioning details, private reviewer contact information, raw simulator captures, and internal App Store identifiers are intentionally excluded.

## Build and archive gates

- Debug iOS Simulator build with Swift and Clang warnings treated as errors
- Release iOS Simulator build with warnings treated as errors
- Release static analysis
- arm64 iOS device archive
- app and widget entitlement inspection
- privacy-manifest validation
- confirmation that local StoreKit testing data and debug premium bypasses were absent from the archive
- strict signature verification of the distribution package

## StoreKit 2 behavior

| Scenario | Expected and verified behavior |
| --- | --- |
| Product loading | Paywall displays the localized one-time StoreKit price |
| Cancellation | Paywall remains usable; no entitlement or false error is created |
| Pending approval | A non-error pending message appears and access remains locked |
| Delayed approval | Transaction update unlocks Verseborne+ and dismisses the paywall |
| Normal purchase | Verified transaction unlocks premium features immediately |
| Restoration | Current entitlements restore access without another purchase |
| Revocation | A verified revoked transaction removes premium access |

## Experience matrix

- iPhone portrait
- iPad portrait and landscape
- accessibility XXXL Dynamic Type
- Reduce Motion with static atmospheric composition
- notification allowed, denied, and manual Settings recovery
- widget small, medium, and large families
- fresh-install free-user flow
- processed TestFlight build on physical iPhone
- Verseborne+ TestFlight purchase and restore

## Submission package

- Public product name and premium name cleared and applied consistently
- World English Bible used for public-domain Scripture quotations
- Font and artwork rights documented
- App icon validated at 1024 × 1024 with no alpha channel
- iPhone and iPad screenshot sets prepared and uploaded
- Support and privacy pages published
- No-data-collected App Privacy disclosure completed
- Free app and $9.99 lifetime in-app purchase submitted together

Verseborne 1.0 was submitted to App Review on September 2, 2026, with manual release selected.
