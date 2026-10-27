# Orbit updates

Signed update feed for [Orbit](https://siosphere.github.io/orbit-updates/), an Arc-style browser.

- `appcast.xml` is the [Sparkle](https://sparkle-project.org) update feed the app checks (at most hourly). It's served by GitHub Pages at https://siosphere.github.io/orbit-updates/appcast.xml.
- App archives are attached to this repo's GitHub Releases.
- Every update is signed with an EdDSA (ed25519) key that lives in AWS Secrets Manager, never in this repo or the app. The app only installs updates whose signature matches the public key built into it.

This repo is published by Orbit's release script; don't edit `appcast.xml` by hand.
