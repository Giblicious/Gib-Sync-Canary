# Gib Sync Canary

Isolated BRAT candidate distribution for disposable test vaults only. Existing
Gib Sync installations must keep tracking
[Giblicious/Gib-Sync](https://github.com/Giblicious/Gib-Sync).

BRAT includes prereleases when choosing updates, so test candidates cannot be
published safely in the production distribution repository.

This repository contains distribution policy, not a separate plugin fork. Its
workflow verifies a successful immutable source release run, source tag/commit,
image digest and every artifact SHA-256 before publishing the exact source-built
bytes. The original source Actions ZIP is retained in an immutable distribution
commit. Its SHA-256 must match GitHub's independently published workflow artifact
digest before extraction, avoiding cross-repository tokens or new secrets. The workflow publishes
release assets; local operators never create or patch a release. It does not
rebuild, alter plugin assets or change production releases.

Do not install this candidate into a real vault. The associated validation server
must enforce its dedicated disposable Seafile account/library; a separate database
alone is insufficient isolation. Physical-device checks must be performed and
reported honestly before the same tested bytes can publish in the production repo.
