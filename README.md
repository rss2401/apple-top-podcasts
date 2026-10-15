# apple-top-podcasts

Apple Podcasts top charts data for [Apple Top](https://github.com/rss2401/apple-top).

This repository only stores data. The website, downloader, and shared workflow live in
[rss2401/apple-top](https://github.com/rss2401/apple-top), which reads this repository's
GitHub Pages site through the relative path `../apple-top-podcasts/`.

## Contents

| Path | Description |
| --- | --- |
| `rankings/YYYYMM/` | Ranking RSS JSON per month: `<country>_podcasts_<feed>.json` |
| `details/<id>.json` | iTunes Lookup responses, one result per country |
| `archives/<id>.json` | Ranking history of each item across months |
| `logos/` | Artwork: `<id>.png` (newest) and `<id>-<url-hash>.png` (versions) |
| `rankings.json` | Index of all ranking and list files, used by the website |

Snapshot at migration: 1318 items, 1291 detail files, 2509 artwork files, 1318 archives.

## Updates

`.github/workflows/update.yml` runs at 03:23 UTC on the first day of each month and every
Monday, and can be started manually. Every run in a month overwrites that month's
`rankings/YYYYMM/` directory, so each month keeps the latest weekly snapshot.

Data before this repository was created was migrated from
[xy2401/appstore](https://github.com/xy2401/appstore), where the full Git history remains.
