# T-companion Android updates

Signed Android trial APKs, update manifests and matching source archives.

Source and build instructions: https://github.com/Jcin004/T-companion

Install over the existing app; export a backup first and retain the original signing key.
No model API keys, conversation data or signing keys belong in this repository.

The direct update manifest is [t-update.json](https://raw.githubusercontent.com/Jcin004/T-companion-updates/main/t-update.json).
It initially matches the existing `android-v0.7.0` Release asset byte for byte;
adding it does not publish a newer APK. T-companion 0.13.2 checks this small file
first, avoiding the Release API and an asset redirect when it is available.

When publishing a newer signed APK and its matching source, replace this file
with that Release's `t-update.json` after verifying the download URL, version code,
APK size and SHA-256. Keep it at the highest published version code, including
trial prereleases. Never point it at a draft or an unpublished APK.
