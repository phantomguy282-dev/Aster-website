# Aster website source

Static marketing/download pages for the Aster browser project.

- Windows installer binaries are intentionally **not** stored in this repository (GitHub rejects files over 100 MB). Distribute installers via GitHub Releases or hosting, then place the file under `downloads/` locally for `verify.cjs` to validate SHA-256/size against `release.json`.
- `node verify.cjs` — structural checks, local links, manifest/installer hash validation.
- `node smoke.cjs` — Playwright layout/error smoke test (requires local `downloads/` file and Edge).
- Mobile section (index.html#mobile) links the verified Android debug APK release: https://github.com/phantomguy282-dev/aster-browser-android/releases/tag/v4.0.0-preview (SHA-256 92ddc82f7c90fd4b9d9633de7ec3dd568a1685cb0a952f4b8bb54da833c18b74).
