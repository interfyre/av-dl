# AV-DL

A cross-platform terminal downloader for videos and other sites, powered by [yt-dlp](https://github.com/yt-dlp/yt-dlp).

## Quick Start

**Windows** — open PowerShell and run:
```powershell
irm dl.interfyre.com | iex
```

**macOS / Linux** — open Terminal and run:
```bash
curl -fsSL dl.interfyre.com/mac | bash
```

No installation required. The script runs entirely from memory and downloads files to your Videos folder (or Movies on macOS).

---

## Menu Options

| Option | Description |
|--------|-------------|
| 1 | Download video + audio as MP4 (best quality) |
| 2 | Download video + audio as MKV (best quality) |
| 3 | Download audio only as MP3 (high quality) |
| 4 | Download audio only as WAV (high quality) |
| 5 | Download audio only (best available format) |
| 6 | Download playlist — organizes each playlist into its own folder |
| 7 | Custom yt-dlp arguments |
| 8 | Install / Update yt-dlp |
| 9 | Check / Install FFmpeg |
| 10 | Install / Update yt-dlp-ejs (YouTube fix) |
| 11 | Check / Install Deno JS Runtime (required for yt-dlp-ejs) |
| 0 | Exit |

---

## Requirements

### Windows
- PowerShell 5.1+ (built into Windows 10/11)
- yt-dlp — install via option 8
- FFmpeg — install via option 9
- Deno — install via option 11 (needed for YouTube EJS support)

### macOS
- Python 3 (pre-installed on macOS)
- yt-dlp — install via option 8
- FFmpeg — install via option 9 (brew install ffmpeg)
- Deno — install via option 11 (brew install deno)

### Linux
- Python 3 (pre-installed on most distros)
- yt-dlp — install via option 8
- FFmpeg — install via your package manager (prompted in option 9)
- Deno — install via option 11

---

## Files

| File | Platform | Purpose |
|------|----------|---------|
| av-dl_v3.ps1 | Windows | Main script |
| av-dl.py | macOS / Linux | Main script |
| install.sh | macOS / Linux | Bootstrap - downloads and runs av-dl.py |

---

## YouTube EJS Fix

Newer versions of yt-dlp require a JavaScript runtime to extract some YouTube formats. If you see the warning:

    No supported JavaScript runtime could be found.

Run options 10 then 11 in that order to install yt-dlp-ejs and Deno.
