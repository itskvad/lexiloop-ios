# Lexiloop iOS builds

Update feed and unsigned iOS builds for the **Lexiloop** app, published by the
`app-lexiloop-ios` Azure Pipeline.

The app's Settings screen reads

    https://github.com/itskvad/lexiloop-ios/releases/latest/download/latest.json

and, when a newer version is published, hands the IPA to TrollStore through
`apple-magnifier://install?url=...`.

## Assets on each release

| Asset | Purpose |
| --- | --- |
| `Lexiloop.ipa` | The unsigned build (ad-hoc signed, no provisioning profile) |
| `latest.json` | Version, build, date, IPA URL and release notes |

`latest.json` looks like this:

```json
{
  "version": "1.2.0",
  "build": "10200",
  "date": "2026-11-18T05:12:00Z",
  "ipa": "https://github.com/itskvad/lexiloop-ios/releases/download/ios-1.2.0/Lexiloop.ipa",
  "notes": "Short summary of what changed."
}
```

## Installing

Open the IPA in TrollStore, or use **Settings → App updates → Check for update**
inside the app. TrollStore must have **URL Scheme Enabled** for the in-app
hand-off to work.

These builds are unsigned; they are not App Store builds and will not install on
a stock, non-jailbroken device.
