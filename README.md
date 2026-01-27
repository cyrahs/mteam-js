# M-Team FREE Torrent Extractor

English | [中文](README_CN.md)

Automatically finds all torrents marked as "FREE" on M-Team pages and fetches download links in bulk via the API.

## Features

- Detects FREE-marked torrents on the page
- Concurrent fetching for faster results (default: 5)
- Copies download links to the clipboard
- Optionally opens a specified URL after copying (e.g., qBittorrent Web UI)
- Real-time progress display
- Customizable API settings

## Configuration

1. Visit M-Team and find the floating button at the bottom-right of the page
2. Click the gear icon button to the right of the main button to open the settings panel
3. Fill in:
   - API Endpoint: `https://api.m-team.cc/api/torrent/genDlToken`
   - API Key (x-api-key): your API key
   - Open URL after copy (optional): e.g. `http://localhost:8080` or `qbittorrent://`
4. Click Save

## Usage

1. Open a page that contains FREE torrents
2. Click the floating button in the bottom-right corner
3. Wait until processing completes (the button shows progress)
4. The download links are copied to the clipboard
5. If configured, the specified URL opens in a new tab after copying

## Button States

- Idle
- Processing (shows progress like 5/10)
- Done (shows success count and copied)
- Not found
- Needs API configuration

## Console Helpers

```javascript
getAllFreeTorrentIds()        // Get all FREE torrent IDs
getMTeamConfig()              // Read current config
showMTeamSettings()           // Open settings panel
window.freeTorrentDownloadLinksArray  // Array of download links
```

## FAQ

Q: No FREE torrents found?
A: Make sure the page is fully loaded, then refresh and try again.

Q: API request failed?
A: Double-check the API Endpoint and API Key, and inspect console errors.

Q: Clipboard copy failed?
A: Check browser clipboard permissions, or copy from console: `window.freeTorrentDownloadLinksArray`
