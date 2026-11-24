# ShadowVPN server release hashes

Public, hashes only. One file per fleet release: `releases/<N>.json`

```json
{"version": N, "commit": "<git commit the release was built from>", "manifest_sha256": "<sha256 of release.json>"}
```

The ShadowVPN Admin app checks a release's manifest against this file before it lets the owner approve
(sign) it. This repo is separate from the website and the database on purpose, so changing one of them
alone can't get a release approved. Only the build machine pushes here. Nothing secret lives in this repo.
