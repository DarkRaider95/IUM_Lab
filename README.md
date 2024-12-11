# Remote File Manager

A simple HTTP-based file manager implemented in Python that allows you to share and access files over a network. This project was developed as part of the Machine Human Interface course to practice Python programming.
It's implemented in Python2 at that time Python3 was in its early days.

## Features

- Web-based file navigation interface
- Cross-platform support (Windows and Linux)
- Simple HTTP server implementation
- File download capabilities
- Directory browsing
- Automatic MIME type detection
- Clean and intuitive user interface
- Drive listing support for Windows systems

## Technical Details

The application consists of several key components:

- `filemanager.py`: Main server implementation that handles socket connections and HTTP requests
- `linman.py`: Linux-specific file management operations
- `winman.py`: Windows-specific file management operations
- Resource files for UI elements (icons and CSS)

The server listens on port 7777 and serves files and directories through a web interface.

## Requirements

- Python (tested on Python 2.x)
- Operating System: Windows or Linux
- Required Python modules:
  - `os`
  - `socket`
  - `string`
  - `platform`
  - `mimetypes`
  - `ctypes` (for Windows only)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/remote-file-manager.git
cd remote-file-manager
```

2. Ensure all resource files are in the correct location:
   - `/resources/directory.png`
   - `/resources/file.png`
   - `/resources/favicon.png`
   - `/resources/fileman.css`

## Usage

1. Start the server:
```bash
python filemanager.py
```

2. Access the file manager through a web browser:
```
http://localhost:7777
```
or from another device on the network:
```
http://[host-ip]:7777
```

## Features in Detail

- **Cross-Platform Compatibility**: Automatically detects the operating system and uses the appropriate file management module
- **Directory Navigation**: Browse through directories with an intuitive interface
- **File Downloads**: Download files directly through the browser
- **Windows Drive Support**: Special support for browsing different drives on Windows systems
- **Error Handling**: Proper error messages for access denied and invalid paths
- **MIME Type Detection**: Automatic detection of file types for proper handling in the browser

## Security Notice

This is a basic implementation meant for educational purposes. It lacks security features that would be necessary for production use, such as:
- Authentication
- Encryption
- Access control
- Input validation

Use this only in trusted networks and for educational purposes.

## Implementation Details

The project uses a basic HTTP server implementation with:
- Socket programming for network communication
- Platform-specific file system operations
- HTML generation for the web interface
- Binary file handling for downloads
- MIME type detection for proper file serving

## License

This project is available for educational purposes. Feel free to use and modify as needed.

## Acknowledgments

Developed as part of the Machine Human Interface course project to practice Python programming skills.