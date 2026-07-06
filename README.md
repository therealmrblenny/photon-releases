# Photon — release channel

Public update manifest for **Photon** (source repo is private).

`version.json` is polled by the app's notify-only update check
(`src/lib/updateCheck.ts`). To announce a new build, bump `version`, refresh
`notes`, and point `url` at where testers can download it, then commit + push.

Manifest URL the app reads (branch-pinned, always latest — **not** the
commit-hashed raw URL):

    https://raw.githubusercontent.com/therealmrblenny/photon-releases/main/version.json

Shape:

    {
      "version": "0.9.9",              // semver of the latest build
      "notes":   "What's new …",       // shown in the update dialog
      "url":     "https://…/download"  // opened when the tester clicks Download
    }

Seeded at 0.9.8 (== current shipped build) so nobody is falsely prompted until
a genuinely newer version is published here.
