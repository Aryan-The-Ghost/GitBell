<div align="center">
  <img src="logo.png" alt="GitBell Logo" width="200"/>
  
  # GitBell
  
  Never miss a GitHub issue again. Get instant notifications when new issues are posted to repositories you track.
  
  <img src="https://img.shields.io/badge/Manifest-V3-blue" alt="Manifest V3"/>
  <img src="https://img.shields.io/badge/Browser-Chrome%20%7C%20Edge-green" alt="Browser Support"/>
</div>

---

## What is GitBell?

A lightweight browser extension that monitors GitHub repositories and alerts you the moment new issues appear. Built for developers who want to stay ahead in open-source contributions, GSoC applications, and project maintenance.

## Features

- Real-time issue monitoring across multiple repositories
- Instant browser notifications with direct links
- Smart detection of beginner-friendly issues
- Configurable check intervals
- Light and dark theme support
- GitHub API token support for higher rate limits
- Clean, minimal interface

## Installation

1. Download or clone this repository
2. Open Chrome/Edge and navigate to `chrome://extensions/`
3. Enable Developer mode
4. Click "Load unpacked" and select the extension directory
5. Start tracking repositories

## Quick Start

Click the extension icon and add repositories in `owner/repo` format:

```
facebook/react
microsoft/vscode
tensorflow/tensorflow
```

Configure your preferences in settings. For best results, add a GitHub Personal Access Token to increase your API rate limit from 60 to 5,000 requests per hour.

## GitHub Token Setup

1. Visit [GitHub Token Settings](https://github.com/settings/tokens/new?scopes=public_repo&description=GitBell)
2. Generate a token with `public_repo` scope
3. Add it in extension settings

## Technical Stack

Built with Manifest V3, Chrome Storage API, Chrome Alarms API, and GitHub REST API v3.

## Rate Limits

| Authentication | Requests/Hour |
|---------------|---------------|
| No Token | 60 |
| With Token | 5,000 |

## Contributing

Contributions are welcome. Check out the issues tab for open tasks or submit your own improvements.

## License

MIT License

---

<div align="center">
  Made with <span style="color: red; font-size: 1.2em;">❤️</span> for the open-source community
</div>
