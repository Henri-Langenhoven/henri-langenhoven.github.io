# Android App Links
* [App Links](https://developer.android.com/training/app-links)
* [Deep Links](https://developer.android.com/training/app-links/deep-linking)
* [Verify App Links (assetlinks.json)](https://developer.android.com/training/app-links/verify-android-applinks)
* [Creating a Statement List (assetlinks.json)](https://developers.google.com/digital-asset-links/v1/create-statement)

# iOS Universal Links
* [Universal Links](https://developer.apple.com/documentation/xcode/allowing-apps-and-websites-to-link-to-your-content)
* [Supporting Universal Links in your App](https://developer.apple.com/documentation/xcode/supporting-universal-links-in-your-app)
* [Associated Domains](https://developer.apple.com/documentation/xcode/supporting-associated-domains)
* [Associated Domains Entitlement](https://developer.apple.com/documentation/bundleresources/entitlements/com_apple_developer_associated-domains)

# Flutter
* [Deep Linking](https://docs.flutter.dev/ui/navigation/deep-linking)
* [Android - App Links](https://docs.flutter.dev/cookbook/navigation/set-up-app-links)
* [iOS - Universal Links](https://docs.flutter.dev/cookbook/navigation/set-up-universal-links)
* [app_links pub.dev package](https://pub.dev/packages/app_links)

# Appendices

## A - Sample [assetlinks.json](https://vitalityfidelidade.page.link/.well-known/assetlinks.json)
```json
[
    {
        "relation":
        [
            "delegate_permission/common.handle_all_urls"
        ],
        "target":
        {
            "namespace": "android_app",
            "package_name": "pt.fidelidade.b2c.vitality",
            "sha256_cert_fingerprints":
            [
                "BB:F5:EA:EA:2D:5C:82:A0:BB:DA:CC:1D:66:48:F8:81:CD:D2:63:0E:F6:94:32:AA:A0:7D:75:0A:EF:64:DC:07",
                "AC:11:5E:54:EC:CF:0E:89:DB:25:BE:97:95:87:11:C0:E0:49:73:59:BC:C1:49:D7:BE:32:F3:25:57:F6:B2:89"
            ]
        }
    },
    {
        "relation":
        [
            "delegate_permission/common.handle_all_urls"
        ],
        "target":
        {
            "namespace": "android_app",
            "package_name": "pt.fidelidade.b2c.vitality.debuggable",
            "sha256_cert_fingerprints":
            [
                "BB:F5:EA:EA:2D:5C:82:A0:BB:DA:CC:1D:66:48:F8:81:CD:D2:63:0E:F6:94:32:AA:A0:7D:75:0A:EF:64:DC:07"
            ]
        }
    }
]
```

## B - Sample [apple-app-site-association](https://vitalityfidelidade.page.link/.well-known/apple-app-site-association)
```json
{
    "applinks":
    {
        "apps":
        [],
        "details":
        [
            {
                "appID": "ADB4VEHB8A.pt.fidelidade.b2c.vitality",
                "paths":
                [
                    "NOT /_/*",
                    "/*"
                ]
            }
        ]
    }
}
```

## C - Sample Android intent-filter
```xml
<intent-filter android:autoVerify="true">
    <action android:name="android.intent.action.VIEW" />
    <category android:name="android.intent.category.DEFAULT" />
    <category android:name="android.intent.category.BROWSABLE" />
    <data android:scheme="https" android:host="vitalityshop.asr.nl" />
    <data android:scheme="https" android:host="asr.ecommerce.test3.sparco.nl" />
</intent-filter>
```