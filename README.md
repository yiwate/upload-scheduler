# Yoake Uploader

A private command-line tool used by one person to publish their own videos to their own
YouTube channels.

**This tool is not distributed.** There is no download, no sign-up, no hosted interface
and no public endpoint. It is not offered to, sold to, or usable by anyone other than its
author. This page exists to document the tool for the YouTube API Services compliance
audit.

## What it does

The tool reads a local JSON configuration file describing one finished video — file path,
title, description, tags, category, thumbnail image and scheduled publish time — and
uploads it to a YouTube channel owned by the author.

It is operated from a terminal on the author's own computer. A `--dry-run` mode prints
exactly what would be sent without calling the API, so every release can be reviewed
before anything is transmitted.

## YouTube API Services used

| API method | Purpose |
|---|---|
| `videos.insert` | Upload a video file owned by the author |
| `thumbnails.set` | Set the custom thumbnail for that video |
| `videos.list` | Read back the author's own video to confirm the upload |
| `playlistItems.insert` | Add the author's own video to the author's own playlist |

No other YouTube API methods are called.

## Data handling

The tool processes **only the author's own content and metadata**. It does not read,
store, display, aggregate or republish data belonging to any other YouTube user or
channel. It performs no search, no analytics on third parties, and no data collection of
any kind from other people.

Authentication uses OAuth 2.0. Tokens are stored locally on the author's own machine and
are never transmitted anywhere except to Google's own API endpoints.

## Channels

The tool publishes to the following channels, all owned and operated by the author:

- https://www.youtube.com/channel/UCPVzN2oKhEN0fZnQQm7rh_A
- https://www.youtube.com/channel/UCQN-I76Jpcgoelq8Mj1LkxA
- https://www.youtube.com/channel/UCvxi4BAL6Cw0UzBTLkazg6w
- https://www.youtube.com/channel/UCcStreZAmI4omy2ua3D1kaA
- https://www.youtube.com/channel/UCg01dhonsMD9FEPm6dr14Pw

## Legal

This tool uses **YouTube API Services**.

- **[Privacy policy](PRIVACY.md)**
- **[Terms of service](TERMS.md)**
| Document | URL |
|---|---|
| **YouTube Terms of Service** | **https://www.youtube.com/t/terms** |
| **Google Privacy Policy** | **https://policies.google.com/privacy** |
| **Revoke this tool's access** | **https://myaccount.google.com/permissions** |

## Contact

aescera@gmail.com
