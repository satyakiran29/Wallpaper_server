# Gwalls Wallpaper Server

A static wallpaper metadata repository for the Gwalls web and mobile experience.

This project stores wallpaper catalogs as JSON files and provides the structure used by Gwalls website and mobile clients to load wallpapers, thumbnails, collections, and depth/live wallpaper content.

## Why this project is useful

- Centralized wallpaper metadata for Gwalls app and website
- Easy to update wallpapers by editing JSON records
- Supports standard wallpapers, live wallpapers, and depth wallpapers
- Works with static hosting and lightweight client apps

## Repository structure

- `gwalls/wallpaper.json` — primary wallpaper catalog for the Gwalls app or desktop site
- `web/mobile/wallpaper.json` — mobile wallpaper catalog for the web client
- `web/mobile/livewallpaper.json` — live wallpaper metadata for mobile clients
- `web/mobile/Moblie_DepthWallpapers.json` — depth wallpaper metadata for mobile clients
- `_github_img/` — repository images used for documentation or site assets

## Getting started

1. Clone the repository:

```bash
git clone https://github.com/<username>/Wallpaper_server.git
cd Wallpaper_server
```

2. Inspect the JSON files to understand the wallpaper schema:

- `gwalls/wallpaper.json`
- `web/mobile/wallpaper.json`
- `web/mobile/livewallpaper.json`
- `web/mobile/Moblie_DepthWallpapers.json`

3. Update or add wallpaper entries using the existing JSON structure.

4. Serve the repository from a static host or use it as a data source for the Gwalls frontend.

## Wallpaper metadata format

Common fields used by the wallpapers in this repository:

- `name` — wallpaper title
- `author` — wallpaper author or source
- `url` — image or video URL for the wallpaper
- `thumbnail` — URL of the thumbnail image
- `collections` — category or collection name
- `copyright` — licensing or usage notes

Depth wallpaper files also include:

- `forground` — foreground image URL
- `background` — background image URL
- `preview` — preview image URL

Live wallpaper files use the same base structure with video URLs.

### Example wallpaper entry

```json
{
  "name": "Rebecca x EdgeRunner 1",
  "author": "Gwalls",
  "url": "https://server.skdev29.workers.dev/0:/GW/Mobile/Random2/R4/W/1.jpg",
  "thumbnail": "https://server.skdev29.workers.dev/0:/GW/Mobile/Random2/R4/P/1.webp",
  "copyright": "Free",
  "collections": "Anime"
}
```

## How to contribute

- Open an issue for bugs, feature requests, or data updates
- Submit a pull request for changes to JSON wallpaper data or repository structure
- Keep payloads valid JSON and preserve the existing field names

## Getting help

- Use the GitHub issue tracker for questions and support
- Review the JSON files in the repository as the primary source of truth

## Notes

- This repository does not include a backend service; it provides wallpaper metadata for Gwalls clients.
- If you want to add new collections, add entries to the appropriate JSON files and verify the data is valid JSON.
