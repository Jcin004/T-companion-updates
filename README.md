# T-companion Android updates

Signed Android trial APKs, update manifests and matching source archives.

Source and build instructions: https://github.com/Jcin004/T-companion

Install over the existing app; export a backup first and retain the original signing key.
No model API keys, conversation data or signing keys belong in this repository.

## Static update manifest

`t-update.json` repeats the manifest for an already published signed release. Update it alongside each new release, after verifying that its APK and corresponding source are available. Android 0.7.1 can use this static file if the Releases API fails, or use an explicitly configured HTTPS manifest. A custom channel must serve a reachable manifest and APK; another GitHub hostname alone does not guarantee connectivity. The app still verifies size, SHA-256, package, version and installed signing identity.
