# De-bloat oneui 9 (Canta Presets)

Canta presets for removing google services, samsung services, general bloatware, tracking components, and other unnecessary system packages from oneui 9.
Only attempts to remove System packages. does not touch packages that can be uninstalled normally.

The goal is to remove as much bloat as possible without ruining the main functionality of the phone. 
## Presets

- [Heavy: 88 packages](preset-heavy.json) - strongest, removes most bloat, google/samsung stuff etc
- [Medium-Heavy: 81 packages](preset-Medium-heavy.json) - like heavy but adds back app stores, gmail & youtube & play services
- [Medium: 69 packages](preset-Medium.json) - like med-heavy but adds back bixby, google, google assistant & samsung cloud

## Compatibility

Intended for samsung devices running oneui 9. If a package isn't present on your phone, Canta will simply skip it.

Tested on:
- Galaxy S24 Ultra (android 17 / oneui 9.0)
- Canta + Shizuku (no root)

**Only apply after completing the initial device setup.**

## Installation

1. install [Canta](https://github.com/samolego/Canta) and [Shizuku](https://github.com/thedjchi/Shizuku).
2. start Shizuku and grant Canta access.
3. open preset-medium.json, press copy raw file.
4. open canta. go to presets > plus > import > import from Clipboard
5. review the selected packages, uninstall, and reboot.

Back up your current Canta configuration before applying the preset if you have one.

## What you lose

heavy is an aggressive debloat preset that removes:

- Google stuff: Google Play Services, Play Store, Google app, ad services, telemetry, and personalization
- Samsung stuff: Bixby, Samsung Pass, Smart Switch, Galaxy Store, cross-device integrations, and other useless features
- Tracking and other bloat: Samsung analytics, personalization, Google tracking components, and preinstalled bloatware and services that cannot normally be uninstalled

It doesn't remove:

- Samsung Keyboard ([choose a better keyboard first](https://github.com/Kirkland-Pickles/Gboard-offline-morphe), then remove it manually)
- Device Care
- Knox components
- oneui updates


The Heavy preset attempts to de-google and de-samsung your device. Some stuff will stop working.

- Samsung Pass (use a [better password manager](https://fmhy.net/internet-tools#password-managers))
- Bixby (use a less [privacy-invasive assistant](https://github.com/DicioTeam/dicio-android))
- Google play services (some apps will stop providing push notification unless [another push noti service is setup](https://unifiedpush.org/))
- Link to Windows and samsung cross-device features (these are privacy nightmares, [alternative](https://kdeconnect.kde.org/))
- Smart Switch (infects your device with old bloat from previous backups)
- Smart Caller ID (invasive Hiya privacy violation)
- Auto Blocker and the google equivalent app scanner (use common sense and VirusTotal)
- Developer verification (Google's verification component removed)

## Restoring packages

Canta uninstalls system packages for the current android user only. It doesn't delete the actual system APKs, so every preset in this repo is reversible and makes no permanent changes to the system partition.

## Disclaimer

Heavy is an aggressive preset intended for people who know what they're removing.

Using it doesn't mean your device is completely free of google or samsung services. This only attempts to remove the stuff that's normally impossible to uninstall. Apps you've installed yourself will still be there.

**Use at your own risk.**
