# ClipboardSnap

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![Platform](https://img.shields.io/badge/platform-macOS-lightgrey)
![Swift](https://img.shields.io/badge/Swift-5.0-orange)

A macOS clipboard history manager with snippet organization, search, and Pro features.

## Features

### Free Features

- 📋 **Automatic Clipboard History** - Tracks everything you copy
- 📌 **Pin Important Items** - Keep frequently used snippets at the top
- 🔍 **Search** - Quickly find items in your clipboard history
- 📤 **Export/Import** - Backup and restore your snippets as JSON
- 🧹 **Auto Cleanup** - Automatically removes oldest unpinned items (keeps last 200)

### Pro Features

- 🏷️ **Multiple Categories** - Organize snippets into categories (Work, Code, Prompt, Personal)
- 🚀 **Future Features** - More Pro features coming soon!

## Installation

**Current Version:** 2.0.0

### Build from Source

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd ClipboardSnap
   ```

2. Open in Xcode:

   ```bash
   open ClipboardSnap.xcodeproj
   ```

3. Build and run:

   - Press `Cmd + R` or click the Run button
   - Or build from terminal:
     ```bash
     xcodebuild -project ClipboardSnap.xcodeproj -scheme ClipboardSnap -configuration Debug build
     ```

4. Run the app:
   ```bash
   open ~/Library/Developer/Xcode/DerivedData/ClipboardSnap-*/Build/Products/Debug/ClipboardSnap.app
   ```

### Checking Version

To check the installed version:

- Open ClipboardSnap
- Go to **ClipboardSnap** menu → **About ClipboardSnap**
- The version number (2.0.0) and build number will be displayed

## How to Use

### Getting Started

1. **Launch the App** - Open ClipboardSnap from Applications or run it from Xcode
2. **Start Copying** - The app automatically tracks everything you copy to the clipboard
3. **View History** - Your clipboard history appears in the main window

### Basic Operations

#### Viewing Clipboard History

- The main window shows all your clipboard history
- **Pinned items** appear at the top in a separate section
- **Recent items** appear below pinned items
- Click on any item to view its full content in the detail pane

#### Copying Items

- **Click an item** in the list to copy it to clipboard
- The item will be marked with a ✓ checkmark when copied
- Use `Cmd + V` to paste in any application

#### Pinning Items

- **Right-click** on any item → Select "Pin"
- Pinned items stay at the top and won't be auto-removed
- To unpin: Right-click → Select "Unpin"

#### Searching

- Use the **search bar** at the top to filter items
- Search matches both content and snippet names
- Search is case-insensitive

### Advanced Features

#### Organizing with Categories (Pro Feature)

1. **Pin an item** first (categories only work for pinned items)
2. **Right-click** the pinned item → Select "Category" → Choose a category
3. **Filter by category** using the sidebar
4. Free users can use **one category**; Pro users can use **multiple categories**

#### Renaming Snippets

1. **Pin an item** first
2. **Right-click** → Select "Rename Snippet…"
3. Enter a short, memorable name
4. The name will appear instead of the content preview

#### Exporting Snippets

1. Click the **menu button** (⋯) in the toolbar
2. Select **"Export Snippets…"**
3. Choose a location and filename
4. Only **pinned snippets** are exported (with names and categories)

#### Importing Snippets

1. Click the **menu button** (⋯) in the toolbar
2. Select **"Import Snippets…"**
3. Choose a JSON file exported from ClipboardSnap
4. Imported items are automatically pinned

#### Clearing History

1. Click the **menu button** (⋯) in the toolbar
2. Select **"Clear History"**
3. Confirm the action
4. **Pinned items are preserved** - only unpinned history is cleared

### Keyboard Shortcuts

#### Navigation

- `↑` / `↓` - Navigate up/down in list
- `Enter` / `Return` - Copy selected item
- `Space` - Copy selected item
- `Esc` - Clear selection or unfocus search

#### Actions

- `Cmd + P` - Pin/unpin selected item
- `Cmd + D` - Delete selected item
- `Cmd + R` - Rename snippet (pinned items only)
- `Cmd + Z` - Undo last delete
- `Cmd + K` - Clear search and focus search field

#### Search

- `Cmd + F` - Focus search field
- `Cmd + G` - Find next (when searching)
- `Cmd + Shift + G` - Find previous (when searching)

#### Categories

- `Cmd + 0` - Show all categories
- `Cmd + 1-4` - Switch to category (Work, Code, Prompt, Personal)

#### Menu

- `Cmd + E` - Export snippets
- `Cmd + I` - Import snippets
- `Cmd + Shift + Delete` - Clear history
- `Cmd + ,` - Open Settings

### Tool Tips

#### Status Indicators

- **📌 Blue pin icon** - Item is pinned
- **✓ Green checkmark** - Last copied item
- **No icon** - Regular unpinned item

#### Context Menu Options

- **Pin/Unpin** - Toggle pin status
- **Rename Snippet…** - Give pinned items custom names (pinned items only)
- **Category** - Assign to category (pinned items only, Pro for multiple)
- **Copy** - Copy item to clipboard
- **Delete** - Remove item from history
- **Undo Delete** - Restore last deleted item (if available)

#### Sidebar

- **All Categories** - Show all items
- **Category names** - Filter by specific category
- Click category to filter items

#### Detail Pane

- Shows full content of selected item
- Displays metadata (character count, word count, line count)
- Text is selectable for copying
- Quick action buttons (Copy, Pin/Unpin, Delete)
- Category and rename options for pinned items
- Visual feedback with toast notifications

## Data Storage

### Location

Clipboard history is stored at:

```
~/Library/Application Support/ClipboardSnap/history.json
```

### Format

The history file is a JSON file containing:

- `history`: Array of clipboard items (most recent first)
- `pinned`: Array of pinned item contents

### Backup

- Use **Export Snippets** to backup your pinned snippets
- The exported file includes names and categories
- Import anytime to restore

## Settings

Access Settings via `Cmd + ,` or from the ClipboardSnap menu.

### General Settings

- **Max Unpinned Items** - Configure how many unpinned items to keep (50-1000, default: 200)
- **Polling Interval** - Adjust how often the app checks for clipboard changes (0.1-2.0 seconds, default: 0.8)

### Appearance Settings

- **Appearance Mode** - Choose System, Light, or Dark mode

### Advanced Settings

- **Data Location** - View where your clipboard history is stored
- **Reveal in Finder** - Open the data folder in Finder
- **Reset All Settings** - Restore default preferences

## Pro Upgrade

### Features Unlocked

- **Multiple Categories** - Use all 4 default categories (Work, Code, Prompt, Personal)
- **Future Features** - Access to upcoming Pro-only features

### How to Upgrade

1. Click the **menu button** (⋯) in the toolbar
2. Select **"Upgrade to Pro…"**
3. Complete the in-app purchase
4. Pro features unlock immediately

## Troubleshooting

### App Not Tracking Clipboard

- Make sure the app has **Accessibility permissions**
- Go to System Settings → Privacy & Security → Accessibility
- Enable ClipboardSnap

### Items Not Appearing

- Check if clipboard contains text (images/files not supported)
- Verify the app is running and not paused
- Try copying something new

### Import/Export Issues

- Ensure you're importing a valid JSON file exported from ClipboardSnap
- Check file permissions
- Verify JSON format (version 2)

### Performance

- The app automatically cleans up old unpinned items (keeps last 200)
- Large clipboard items may take longer to process
- Import size limit: 50,000 characters per item

## Development

### Project Structure

```
ClipboardSnap/
├── ClipboardSnapApp.swift      # App entry point
├── ContentView.swift            # Main UI
├── ClipboardViewModel.swift    # View model and business logic
├── ClipboardManager.swift      # Clipboard monitoring and persistence
├── UserDefaultsManager.swift   # User preferences management
├── SettingsView.swift          # Settings/Preferences window
├── ToastView.swift             # Toast notification system
├── AboutView.swift             # About window
└── Constants.swift             # Configuration constants
```

### Requirements

- macOS 13.0 or later
- Xcode 14.0 or later
- Swift 5.0 or later

## App Store Submission

For detailed guides on preparing for App Store submission, see:

- **[Quick Start Guide](QUICK_START_APP_STORE.md)** - Step-by-step submission process
- **[App Store Checklist](APP_STORE_CHECKLIST.md)** - Complete checklist
- **[Icon Guide](ICON_GUIDE.md)** - App icon requirements and setup
- **[Bundle ID Guide](BUNDLE_ID_GUIDE.md)** - Bundle ID configuration
- **[StoreKit Setup](STOREKIT_SETUP.md)** - In-app purchase configuration
- **[Contact Info Template](CONTACT_INFO_TEMPLATE.md)** - Where to add contact information
- **[Implementation Summary](IMPLEMENTATION_SUMMARY.md)** - Technical implementation details

### Version Information

- **Current Version:** 2.0.0
- **Build Number:** 1
- Version can be viewed in the About window (ClipboardSnap menu → About ClipboardSnap)

### Building

```bash
# Debug build
xcodebuild -project ClipboardSnap.xcodeproj -scheme ClipboardSnap -configuration Debug build

# Release build
xcodebuild -project ClipboardSnap.xcodeproj -scheme ClipboardSnap -configuration Release build
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, bug reports, or feature requests:
- Open an issue on GitHub (if applicable)
- Contact through App Store support page

## Contact

For support, bug reports, or feature requests:
- Email: [Add your email here]
- App Store: Support page (after publication)
- Website: [Add your website here] (optional)

## Privacy & Legal

- [Privacy Policy](PrivacyPolicy.md) - How we handle your data
- [Terms of Service](TERMS.md) - Terms and conditions

**Key Points:**

- All data stays on your device
- No data transmission to external servers
- No analytics or tracking
- Full control over your data

## Changelog

### Version 2.0.0

- Converted from menu bar app to full application
- Added SwiftUI interface with sidebar and detail view
- Improved organization with categories
- Enhanced search functionality
- Better error handling
- Added About window with version information
- Improved code organization and maintainability
- **New in 2.0.0:**
  - Settings window with configurable options
  - Toast notifications for user actions
  - Undo functionality for delete actions
  - Enhanced UI with animations and visual feedback
  - Improved error messages and user feedback
  - Better empty states
  - Privacy policy and terms of service
  - **App Store Ready Features:**
    - StoreKit integration for in-app purchases
    - Accessibility permission handling with user-friendly UI
    - Pro upgrade system with purchase flow
    - Restore purchases functionality
    - Complete Info.plist with privacy descriptions
    - App Store submission checklist

### Version 1.0.0

- Initial release as menu bar app
- Basic clipboard history tracking
- Pin/unpin functionality
- Export/import snippets
