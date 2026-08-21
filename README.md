# AxzoraOS OTA

Release assets (APKs) served over-the-air to installed AxzoraOS phones.
The private `axzora-server` redirects `/update/download` to the asset named
in its `update/update.json`. Big binaries live here as Release assets
(2 GB/asset limit) — never committed to the repo tree.
