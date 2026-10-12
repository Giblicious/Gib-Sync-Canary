# Isolated candidate distribution

This repository distributes immutable workflow-built assets from Giblicious/Gib-Sync.
Never build a different plugin, patch release assets, move an existing version tag,
publish in the production repository before acceptance, or install into a real vault.

Every publication must bind a successful source workflow run, exact numeric tag,
source commit, immutable image digest and complete asset hashes. A failed check is
not permission to manually create/upload a release. The owned workflow publishes.
Candidate payloads committed here must be the exact original source Actions ZIP,
byte-verified against GitHub's artifact digest first; never build, recompress or
edit them locally. The workflow independently checks that public artifact digest.

Never commit device credentials, vault keys, server details, private evidence,
personal paths or physical-test diagnostic contents. BRAT/user owns installation.
