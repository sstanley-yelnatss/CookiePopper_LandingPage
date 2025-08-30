# 🍪 CookiePopper

Automatically detect and dismiss cookie consent banners to save you time and reduce browsing friction.

## ✨ Features

- **Automatic Banner Detection**: Detects cookie banners on 85%+ of websites
- **Smart Dismissal**: Automatically clicks accept/agree buttons or hides banners
- **Cross-Browser Support**: Works on Chrome, Firefox, and Edge
- **Privacy-First**: No personal data collection, everything stored locally
- **Performance Optimized**: <50ms detection time, <5MB memory footprint
- **Freemium Model**: 14-day free trial, then upgrade to Pro for unlimited access

## 🚀 Install CookiePopper

### 🌐 Chrome Users
1. Visit the [Chrome Web Store](https://chrome.google.com/webstore) (coming soon!)
2. Search for "CookiePopper"
3. Click "Add to Chrome"
4. Confirm the installation

### 🦊 Firefox Users
1. Visit [Firefox Add-ons](https://addons.mozilla.org) (coming soon!)
2. Search for "CookiePopper"
3. Click "Add to Firefox"
4. Confirm the installation

### 🔷 Edge Users
1. Visit the [Edge Add-ons Store](https://microsoftedge.microsoft.com/addons) (coming soon!)
2. Search for "CookiePopper"
3. Click "Get"
4. Confirm the installation

### 📱 After Installation
- CookiePopper will automatically detect and dismiss cookie banners
- Click the extension icon to toggle on/off
- Right-click the icon to access settings
- No configuration needed - works out of the box!

---

## 🛠️ For Developers

### Prerequisites
- Node.js 18+ and npm 8+
- Chrome, Firefox, or Edge browser

### Build from Source

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/cookiepopper.git
   cd cookiepopper
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Build for your browser**
   ```bash
   # For Chrome
   npm run build:chrome
   
   # For Firefox
   npm run build:firefox
   
   # For Edge
   npm run build:edge
   ```

4. **Load the extension for development**
   ```bash
   npm run dev:chrome  # Follow the instructions displayed
   ```

### Development Server

Start the development server with hot reload:

```bash
npm run dev
```

This starts webpack dev server on `https://localhost:9000` with:
- Hot reload for all file changes
- HTTPS (required for extension permissions)
- Source maps for debugging

### Building

```bash
# Development build
npm run build

# Browser-specific builds
npm run build:chrome
npm run build:firefox
npm run build:edge

# Production build with optimization
npm run build
```

### Testing

```bash
# Unit tests
npm run test

# Watch mode
npm run test:watch

# End-to-end tests
npm run test:e2e
```

### Code Quality

```bash
# Lint code
npm run lint

# Fix linting issues
npm run lint:fix

# Type checking
npm run type-check
```

## 📁 Project Structure

```
src/
├── background/          # Service worker
├── content/            # Content scripts
├── popup/              # Extension popup UI
├── options/            # Settings page
├── manifest/           # Browser-specific manifests
└── assets/             # Icons and assets

webpack/                # Build configuration
├── webpack.common.js   # Common config
├── webpack.dev.js      # Development config
└── webpack.prod.js     # Production config

scripts/                # Build and development scripts
```

## 🔧 Configuration

### TypeScript

The project uses strict TypeScript configuration with:
- ES2020 target
- Strict type checking
- Path aliases (`@/` for `src/`)
- Chrome extension types

### Webpack

- **Development**: Hot reload, source maps, HTTPS server
- **Production**: Minification, optimization, chunk splitting
- **Browser Support**: Chrome, Firefox, Edge builds

## 🌐 Browser Support

| Browser | Version | Status |
|---------|---------|---------|
| Chrome  | 88+     | ✅ Full Support |
| Firefox | 85+     | ✅ Full Support |
| Edge    | 88+     | ✅ Full Support |

## 📱 Extension Components

### Background Service Worker
- Manages extension state
- Handles storage operations
- Processes messages from content scripts
- Updates extension badge

### Content Scripts
- Detects cookie banners using CSS selectors
- Implements dismissal strategies
- Observes DOM changes for dynamic content
- Communicates with background service

### Popup UI
- Quick enable/disable toggle
- Status indicators
- Manual dismissal options
- Statistics display

### Options Page
- Detailed settings configuration
- Site-specific rules
- Dismissal history
- Performance metrics

## 🎯 Banner Detection

The extension detects banners using multiple strategies:

1. **CSS Selectors**: Common banner frameworks (OneTrust, Cookiebot, etc.)
2. **Text Patterns**: Cookie-related keywords and consent language
3. **DOM Structure**: Banner-like element patterns
4. **Fallback Detection**: Generic banner identification

## 🚀 Deployment

### Chrome Web Store
1. Build: `npm run build:chrome`
2. Package: `npm run package`
3. Upload to [Chrome Web Store](https://chrome.google.com/webstore/devconsole)

### Firefox Add-ons
1. Build: `npm run build:firefox`
2. Package: `npm run package`
3. Submit to [Firefox Add-ons](https://addons.mozilla.org/developers/)

### Edge Add-ons
1. Build: `npm run build:edge`
2. Package: `npm run package`
3. Submit to [Edge Add-ons](https://partner.microsoft.com/dashboard/microsoftedge/)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Browser extension community
- Open source contributors
- Privacy advocates

---

**Made with ❤️ for a better browsing experience**
