# YouTube Adfree Player

A lightweight desktop application for playing YouTube videos using MPV player with a modern GUI interface.

## Screenshot
![Screenshot](res/screenshot.png)

## Features

- 🎥 Play YouTube videos, playlists, and live streams
- 🖥️ Fullscreen support
- 🔄 Loop playback option
- 📋 Quick paste from clipboard
- 📜 URL history tracking
- ⚙️ Configurable settings
- 🔄 Automatic yt-dlp updates

## Requirements

- Python 3.7+
- MPV player
- yt-dlp

### Python Dependencies

```bash
pip install PyQt6 pyperclip
```

## Project Structure

```
project/
├── src/
│   ├── main.py
│   ├── config.ini (auto-generated)
│   └── history.json (auto-generated)
├── tools/
│   ├── mpv.exe
│   └── yt-dlp.exe
└── logs/
```

## Installation

1. Clone or download this repository
2. Install Python dependencies:
   ```bash
   pip install PyQt6 pyperclip
   ```
3. Download [MPV player](https://mpv.io/installation/) and place `mpv.exe` in the `tools/` folder
4. Download [yt-dlp](https://github.com/yt-dlp/yt-dlp/releases) and place `yt-dlp.exe` in the `tools/` folder

## Usage

### Running from Source

```bash
python src/main.py
```

### Building Executable

Using PyInstaller:
```bash
pip install pyinstaller
pyinstaller --onefile --windowed  --icon=res/icon.ico --name "YouTube Player" src/main.py  
```

Place the resulting executable alongside the `tools/` folder.

## Configuration

Settings can be configured via the Settings dialog (⚙️ button):

- **MPV Player Path**: Location of mpv.exe
- **YT-DLP Path**: Location of yt-dlp.exe
- **Log Directory**: Where log files are saved
- **Max History Items**: Number of URLs to remember (1-100)

Configuration is automatically saved to `config.ini`.

## Keyboard Shortcuts

- **Ctrl+P**: Play video
- **Escape**: Stop playback

## Supported URLs

- Standard videos: `youtube.com/watch?v=...`
- Short URLs: `youtu.be/...`
- Shorts: `youtube.com/shorts/...`
- Playlists: `youtube.com/playlist?list=...`
- Live streams: `youtube.com/live/...`

## Logging

Application logs are saved to the configured log directory with timestamps:
```
logs/youtube_player_YYYYMMDD_HHMMSS.log
```

## License

This project is provided as-is for personal use.

## Credits

- [MPV Media Player](https://mpv.io/)
- [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- Built with PyQt6