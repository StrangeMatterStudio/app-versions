# app-versions

The latest TestFlight build of each Strange Matter Studios app, keyed by bundle id. The release scripts update
`versions.json` after every successful upload; nothing else writes it.

Apps installed from TestFlight read
`https://raw.githubusercontent.com/StrangeMatterStudio/app-versions/main/versions.json` at launch. If the installed
version is older than `testflight.version` (or the same version with a lower build), they show the forced update card,
whose Update button opens the TestFlight app. App Store installs never use this file; they compare against the App
Store's own lookup. An app removes its TestFlight check once it is live on the App Store.

Only version numbers live here. Never add secrets, user data or unreleased feature names.
