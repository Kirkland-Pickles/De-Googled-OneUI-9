# De-bloat oneui 9 (Canta Presets)

Canta presets for removing google services, samsung services, general bloatware, tracking components, and other unnecessary system packages from oneui 9.

The goal is to remove as much bloat as possible without ruining the main functionality of oneui.

## Presets (currently just one)

### [Heavy: 84 packages](preset-heavy.json)

Aggressive debloat preset that removes:

- Google stuff: Google Play Services, Play Store, Google app, ad services, telemetry, and personalization
- Samsung stuff: Bixby, Samsung Pass, Smart Switch, Galaxy Store, cross-device integrations, and other useless features
- Tracking and other bloat: Samsung analytics, personalization, Google tracking components, and preinstalled bloatware and services that cannot normally be uninstalled

It doesn't remove:

- Samsung Keyboard ([choose a better keyboard first](https://github.com/Kirkland-Pickles/Gboard-offline-morphe), then remove it manually)
- Device Care
- Knox components
- oneui system updates

## Compatibility

Intended for samsung devices running oneui 9. If a package isn't present on your phone, Canta will simply skip it.

Tested on:
- Device: Galaxy S24 Ultra (android 17 / oneui 9.0)
- Method: Canta + Shizuku (no root)

Other oneui 9 devices may work but haven't been tested.

**Only apply after completing the initial device setup.**

## Installation

1. Install [Canta](https://github.com/samolego/Canta) and [Shizuku](https://github.com/thedjchi/Shizuku).
2. Start Shizuku and grant Canta access.
3. open preset-heavy.json, press copy raw file.
4. open canta. go to presets > plus > import > import from Clipboard
5. Review the selected packages, uninstall, and reboot.

Back up your current Canta configuration before applying the preset if you have one.

## What you lose

The Heavy preset attempts to de-google and de-samsung your device. Some stuff will stop working.

- Google Play Services
- Play Store
- Galaxy Store
- Samsung Pass (use a better password manager)
- Bixby (use a less privacy-invasive assistant)
- Link to Windows and samsung cross-device features (these are privacy nightmares)
- Smart Switch (infects your device with old bloat from previous backups)
- Smart Caller ID (invasive Hiya privacy violation)
- Auto Blocker and the google equivalent app scanner (use common sense and VirusTotal)
- Developer verification (Google's verification component removed)

## Restoring packages

Canta uninstalls system packages for the current android user only. It doesn't delete the actual system APKs, so every preset in this repo is reversible and makes no permanent changes to the system partition.

## Disclaimer

This is an aggressive preset intended for people who know what they're removing.

Using it doesn't mean your device is completely free of google or samsung services. This only attempts to remove the stuff that's normally impossible to uninstall. Apps you've installed yourself will still be there.

**Use at your own risk.**
