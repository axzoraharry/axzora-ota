# AxzoraOS OTA

Release assets (APKs) served over-the-air to installed AxzoraOS phones.
The private `axzora-server` redirects `/update/download` to the asset named
in its `update/update.json`. Big binaries live here as Release assets
(2 GB/asset limit) — never committed to the repo tree.

## Latest

| | |
| --- | --- |
| Version | **18.18** (`versionName`) |
| Version code | **210** |
| Asset | [`AxzoraOS-18.18.apk`](https://github.com/axzoraharry/axzora-ota/releases/download/v18.18/AxzoraOS-18.18.apk) — 109,175,671 bytes |
| sha256 | `1d0ae458d93dfdd04938b11da818ed4581e3ff6530fd13e3e14cd6306a43bcc4` |
| Signing | v2 + v3, `F9276561428321C0D28A98E3B95B8463DE656370625944FF0280C351C8790456` |
| Notes | Hub panel: editable endpoint, one-tap test, latency history, live OTA readout |

`/update/check` response:

```json
{
  "ok": true,
  "versionCode": 210,
  "versionName": "18.18",
  "file": "AxzoraOS-18.18.apk",
  "url": "https://github.com/axzoraharry/axzora-ota/releases/download/v18.18/AxzoraOS-18.18.apk"
}
```

## Install

Download the `.apk` and open it. Android verifies that the signature matches
the installed copy and installs **in place** — settings, history and pairing
survive. Installed phones are offered the same build automatically on launch.

Every build is signed with the same long-lived release key, so
`versionCode` must always increase; Android refuses a downgrade.

## Release history

| Tag | Code | Headline |
| --- | --- | --- |
| [v18.18](https://github.com/axzoraharry/axzora-ota/releases/tag/v18.18) | 210 | Hub panel — latency, history, live OTA channel |
| [v18.16](https://github.com/axzoraharry/axzora-ota/releases/tag/v18.16) | 96 | Omarchy terminal home |
| [v18.15](https://github.com/axzoraharry/axzora-ota/releases/tag/v18.15) | 95 | Titled TUI frames, pinned favourites |
| [v18.14](https://github.com/axzoraharry/axzora-ota/releases/tag/v18.14) | 94 | Command-bar calculator |
| [v18.13](https://github.com/axzoraharry/axzora-ota/releases/tag/v18.13) | 93 | Waybar workspaces |
| [v18.12](https://github.com/axzoraharry/axzora-ota/releases/tag/v18.12) | 92 | Fastfetch system card |
| [v18.11](https://github.com/axzoraharry/axzora-ota/releases/tag/v18.11) | 91 | Swipe gestures |
| [v18.10](https://github.com/axzoraharry/axzora-ota/releases/tag/v18.10) | 90 | Terminal home groundwork |

Codes 90–96 came from a separate numbering line; the 18.17+ builds resume at
209/210 so they rank above every build already on a phone.
