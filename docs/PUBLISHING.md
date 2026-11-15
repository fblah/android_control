# Distribution policy

This repository is public. Include only public user documentation and approved release outputs.

Allowed release assets: signed generic APKs, signed update manifests, checksums, and sanitized release notes.

Exclude private development source, deployment settings, internal infrastructure addresses, credentials, signing keys, device identifiers, real QR invitations, and private logs. Publish from the protected private release pipeline; do not mirror the development repository.

Repository visibility does not protect a secret once it is embedded in an APK. Inspect release outputs before publication.
