<div align="center">
  <img src="logo.png" alt="GitBell Logo" width="200"/>
  
  # GitBell
  
  Get notified when new issues are posted to GitHub repositories you track.
  
  <img src="https://img.shields.io/badge/Manifest-V3-blue" alt="Manifest V3"/>
  <img src="https://img.shields.io/badge/Browser-Chrome%20%7C%20Edge-green" alt="Browser Support"/>
</div>

---

## About

GitBell is a browser extension that monitors GitHub repositories and sends instant notifications when new issues are created. Perfect for GSoC contributors, open-source maintainers, and developers who want to stay on top of repository activity.

## Features

- Real-time monitoring of multiple repositories
- Browser notifications for new issues
- Configurable check intervals (5-30 minutes)
- GitHub API token support for higher rate limits
- Smart detection of beginner-friendly issues
- Clean, minimalistic interface
- Statistics dashboard

## Installation

### Chrome / Edge

1. Navigate to `chrome://extensions/` or `edge://extensions/`
2. Enable **Developer mode**
3. Click **Load unpacked**
4. Select the extension directory

## Usage

### Adding Repositories

Click the extension icon and enter repositories in `owner/repository` format:

```
facebook/react
tensorflow/tensorflow
kubernetes/kubernetes
```

### Configuring Settings

Access settings via the gear icon to:
- Add GitHub Personal Access Token (optional, increases rate limit from 60 to 5,000 requests/hour)
- Set check interval
- Configure notification preferences

### Generating GitHub Token

1. Visit [GitHub Token Settings](https://github.com/settings/tokens/new?scopes=public_repo&description=GitBell)
2. Select `public_repo` scope
3. Generate and copy token
4. Paste in extension settings

## Technical Details

**Built with:**
- Manifest V3
- Chrome Storage API
- Chrome Alarms API
- Chrome Notifications API
- GitHub REST API v3

**Permissions:**
- `storage` - Save repositories and settings
- `notifications` - Display new issue alerts
- `alarms` - Schedule periodic checks
- `https://api.github.com/*` - Access GitHub API

## File Structure

```
extension/
├── manifest.json       # Extension configuration
├── background.js       # Service worker
├── storage.js         # Storage utilities
├── github-api.js      # GitHub API integration
├── popup.html/css/js  # Main interface
├── settings.html/css/js # Settings page
└── icons/             # Extension icons
```

## API Rate Limits

| Authentication | Requests/Hour | Use Case |
|---------------|---------------|----------|
| No Token | 60 | 1-6 repositories |
| With Token | 5,000 | Unlimited repositories |

## Contributing

Contributions are welcome. Feel free to open issues or submit pull requests.

## License

MIT License

---

<div align="center">
  Made for the open-source community
</div>
