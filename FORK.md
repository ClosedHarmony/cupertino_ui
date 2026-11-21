# OpenHarmony adaptation

This package follows the published `cupertino_ui 1.1.7` release, with Dart 3.13
and Flutter 3.47 as its minimum toolchain. The release archive SHA-256 is
`c3eaf7f5bdfee36deb0b14a4cbf7602f1b6b8d8b8576b81f38fc08c25881c94c`.

OpenHarmony Flutter adds `TargetPlatform.ohos`. Exhaustive platform switches
include that value alongside Android for non-Apple behaviour. These cases
cannot compile against the official Flutter enum, so the application selects
this fork only for OHOS and keeps the same package version as its standard
builds.

When syncing a release, compare `lib/` against the published archive and retain
only the OHOS platform cases. Validate the package through the application's
HAP build with its matching `material_ui` fork.
