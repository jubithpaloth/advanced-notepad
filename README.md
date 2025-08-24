# Advanced Local Notepad

A powerful, feature-rich notepad application that runs entirely in your browser with no server required. Perfect for local file editing, note-taking, and text manipulation.

<img width="1913" height="946" alt="image" src="https://github.com/user-attachments/assets/076e314b-64c5-4969-946a-04c08a00c467" />

## ✨ Features

### 📝 **Multi-Note Management**
- Create, edit, and organize multiple notes
- Search across all notes
- Pin important notes to the top
- Auto-save with local storage persistence

### 🔧 **Advanced Text Editing**
- Line numbers with gutter
- Duplicate line (`Dup Line` button)
- Delete line (`Del Line` button)
- Tab indentation support
- Word wrap toggle
- Spellcheck toggle
- Adjustable font size (11-22px)

### 🔍 **Find & Replace**
- Real-time search highlighting
- Case-sensitive search option
- Whole word matching
- Regular expression support
- Replace and Replace All functionality

### 📁 **File Operations**
- **Open**: Load text files (.txt, .md, .log, .csv, .json)
- **Save**: Download current note as .txt file
- **Save As**: Save with custom filename
- **Print**: Print current note with proper formatting
- **Export**: Backup all notes to JSON file
- **Import**: Restore notes from JSON backup

### 🎨 **Customization**
- Dark/Light theme toggle
- Resizable sidebar
- Persistent preferences
- Monospace font optimized for coding

### ⌨️ **Keyboard Shortcuts**
- `Ctrl/Cmd + S` - Save current note
- `Ctrl/Cmd + Shift + S` - Save As
- `Ctrl/Cmd + O` - Open file
- `Ctrl/Cmd + P` - Print
- `Ctrl/Cmd + F` - Find & Replace
- `Ctrl/Cmd + N` - New note
- `Ctrl/Cmd + K` - Search notes
- `Ctrl/Cmd + B` - Toggle sidebar
- `Ctrl/Cmd + /` - Toggle word wrap
- `Esc` - Close find bar

## 🚀 Quick Start

### Method 1: Direct File Access
1. Download `NotePad.html`
2. Open in any modern browser
3. Start typing immediately!

### Method 2: Local Server (Recommended for FS API)
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve

# Then open: http://localhost:8000/NotePad.html
```

### Method 3: Online Hosting
- Upload to GitHub Pages, Netlify, or any web host
- Access via HTTPS for full FS API support

## 🔐 File System Access API

The notepad supports the modern File System Access API for enhanced file operations:

| Environment | FS API Status | Features Available |
|-------------|---------------|--------------------|
| `file://` protocol | ❌ No | Basic download/upload |
| `http://localhost` | ✅ Yes* | Direct file system access |
| `https://` sites | ✅ Yes* | Direct file system access |

*In Chromium-based browsers (Chrome, Edge, Opera)

## 📋 File Operations Explained

### Single Note Operations
- **Open** 📂 - Import a text file as a new note
- **Save** 💾 - Download current note as .txt
- **Save As** 💾 - Download with custom filename
- **Print** 🖨️ - Print current note

### Bulk Operations  
- **Export** 📦 - Backup ALL notes to JSON
- **Import** 📥 - Restore notes from JSON backup

## 🎯 Use Cases

### For Developers
- Quick code snippets and notes
- Log file viewing and analysis
- Configuration file editing
- Markdown documentation

### For Writers
- Draft articles and stories
- Note organization and research
- Text formatting and editing
- Multiple document management

### For Students
- Lecture notes and study materials
- Assignment drafts
- Research organization
- Quick calculations and lists

## 🌐 Browser Compatibility

| Browser | Basic Features | FS API | Status |
|---------|---------------|---------|---------|
| Chrome 86+ | ✅ | ✅ | Fully supported |
| Edge 86+ | ✅ | ✅ | Fully supported |
| Opera 72+ | ✅ | ✅ | Fully supported |
| Firefox | ✅ | ❌ | Basic features only |
| Safari | ✅ | ❌ | Basic features only |

## 💾 Data Storage

- **Local Storage**: All notes stored in browser's localStorage
- **No Cloud**: Complete privacy - data never leaves your device
- **Portable**: Export/import for backup and transfer
- **Persistent**: Notes survive browser restarts

## 🛠️ Technical Details

### Built With
- **Vanilla JavaScript** - No frameworks or dependencies
- **Modern CSS** - CSS Grid, Flexbox, Custom Properties
- **Web APIs** - File System Access, Local Storage, Blob


### Key Components
- **State Management** - Centralized application state
- **Event Handling** - Comprehensive keyboard and mouse support
- **File Operations** - Robust file I/O with fallbacks
- **Search Engine** - Real-time text search with highlighting
- **Theme System** - Dynamic light/dark mode switching

## 🔧 Customization

### Themes
The notepad includes built-in dark and light themes. You can customize colors by modifying CSS custom properties:

```css
:root {
  --bg: #0b0f14;          /* Background color */
  --text: #e6edf3;        /* Text color */
  --accent: #4aa3ff;      /* Accent color */
  /* ... more variables */
}
```

### Features Toggle
Enable/disable features by modifying the JavaScript configuration:

```javascript
const state = {
  wrap: true,           // Word wrap
  spell: true,          // Spellcheck
  theme: 'dark',        // Default theme
  fontSize: 14          // Default font size
};
```

## 📝 Tips & Tricks

### Productivity Tips
1. **Use keyboard shortcuts** for faster navigation
2. **Pin frequently used notes** to keep them at the top
3. **Use search** to quickly find content across all notes
4. **Export regularly** to backup your work
5. **Try regex search** for powerful text matching

### File Management
1. **Name your notes descriptively** for better organization
2. **Use Export/Import** to sync between devices
3. **Save important notes** as .txt files for external access
4. **Use Print** to create physical copies

### Advanced Usage
1. **Regular expressions** in find/replace for complex text manipulation
2. **Markdown support** - write in Markdown, export as .md files
3. **Code editing** - syntax-friendly with monospace font and line numbers
4. **Log analysis** - open large log files for inspection

## 🐛 Troubleshooting

### Common Issues

**Q: Buttons not working?**
A: Check browser console (F12) for errors. Try refreshing the page.

**Q: Can't open files?**
A: Ensure you're using a supported browser. For FS API, use localhost or HTTPS.

**Q: Notes disappeared?**
A: Check if localStorage is enabled. Try importing from a JSON backup.

**Q: Search highlighting misaligned?**
A: This was fixed in the latest version. Refresh or re-download the file.

**Q: Print not working?**
A: Disable popup blockers for the notepad domain.

### Performance
- The notepad can handle files up to several MB in size
- Search performance may slow with very large notes (>1MB)
- Recommend splitting large documents into multiple notes

## 🤝 Contributing

This is a single-file application designed for simplicity. To contribute:

1. **Test thoroughly** across different browsers
2. **Maintain single-file architecture** - no external dependencies
3. **Preserve backward compatibility** with existing saved notes
4. **Follow existing code style** and patterns

## 📜 License

MIT License - Free to use, modify, and distribute.

## 🔗 Links

- **Issues & Feedback**: Report bugs or request features
- **Documentation**: This README covers all functionality
- **Updates**: Check for new versions periodically

---

**Made with ❤️ for developers, writers, and anyone who loves a good notepad!**

*Last updated: August 2025*
