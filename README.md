# MDU Online Installer

A lightweight online installer for Media Downloader Utility (MDU) that automatically fetches and installs the latest version.

## Features

- 🚀 Automatic latest version detection from GitHub
- 📦 Downloads and installs the full package
- 🔄 Auto-updates from previous versions
- 🛡️ Requires admin privileges for proper installation
- 💻 Clean and modern interface
- 📊 Real-time download progress
- 🔍 Version checking and compatibility

## Installation

1. Download the installer:
   - [Download Latest Installer](https://github.com/project-mdu/mdu-installer/releases/latest)

2. Run the installer:
   - Right-click `mdu_setup.exe`
   - Select "Run as administrator"
   - Follow the on-screen instructions

## Build from Source

### Prerequisites

```bash
# Install required packages
pip install -r requirements.txt
```

Required packages:
- PySide6>=6.5.0
- requests>=2.31.0
- pywin32>=305
- pyinstaller>=6.2.0

### Building

```bash
# Build using spec file
pyinstaller --clean mdu_setup.spec
```

Or use direct command:
```bash
pyinstaller --clean --windowed --onefile --icon=icon.ico --name=mdu_setup --version-file=file_version_info.txt installer.py
```

## Project Structure

```
mduonlineinstaller/
├── installer.py          # Main installer code
├── icon.ico             # Application icon
├── mdu_setup.spec       # PyInstaller specification
├── file_version_info.txt # Windows version info
├── requirements.txt     # Python dependencies
├── screenshots/         # Screenshots for documentation
└── README.md           # This file
```

## Installation Location

The application installs to:
```
%LOCALAPPDATA%\kaoniewji\Media Downloader Utility
```

## Features in Detail

### Auto-Update System
- Checks GitHub for latest release
- Compares with installed version
- Downloads updates automatically

### Uninstallation Support
- Removes previous versions
- Cleans registry entries
- Removes desktop shortcuts
- Closes running instances

### User Interface
- Progress tracking
- Status messages
- Release notes display
- Version information

## Development

### Building New Release

1. Update version information:
   ```python
   # file_version_info.txt
   filevers=(2024, 12, 22, 0)
   prodvers=(2024, 12, 22, 0)
   ```

2. Build installer:
   ```bash
   pyinstaller --clean mdu_setup.spec
   ```

3. Test installation:
   - Clean install
   - Update from previous version
   - Uninstall

### Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [PySide6](https://wiki.qt.io/Qt_for_Python)
- Packaging by [PyInstaller](https://www.pyinstaller.org/)
- Icon resources from [Icons8](https://icons8.com/)

## Support

For support, please:
1. Check existing [Issues](https://github.com/project-mdu/mdu-installer/issues)
2. Create a new issue if needed
3. Join our [Discord](https://discord.gg/your-server)

## Release Notes

### v2024.12.22 LTS
- Initial release of online installer
- Automatic update system
- Modern UI design
- Admin privileges handling
- Improved error handling

---
Made with ❤️ by [kaoniewji](https://github.com/kaoniewji)
