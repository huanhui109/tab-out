# Tab Out

**Keep tabs on your tabs.**

Tab Out is a Chrome extension that replaces your new tab page with a dashboard of everything you have open. Tabs are grouped by domain, with homepages (Gmail, X, LinkedIn, etc.) pulled into their own group. Close tabs with a satisfying swoosh + confetti.

No server. No account. No external API calls. Just a Chrome extension.

---

## Install with a coding agent

Send your coding agent (Claude Code, Codex, etc.) this repo and say **"install this"**:

```
https://github.com/zarazhangrui/tab-out
```

The agent will walk you through it. Takes about 1 minute.

---

## Features

- **See all your tabs at a glance** on a clean grid, grouped by domain
- **Homepages group** pulls Gmail inbox, X home, YouTube, LinkedIn, GitHub homepages into one card
- **Close tabs with style** with swoosh sound + confetti burst
- **Duplicate detection** flags when you have the same page open twice, with one-click cleanup
- **Click any tab to jump to it** across windows, no new tab opened
- **Save for later** bookmark tabs to a checklist before closing them
- **Localhost grouping** shows port numbers next to each tab so you can tell your vibe coding projects apart
- **Expandable groups** show the first 8 tabs with a clickable "+N more"
- **100% local** your data never leaves your machine
- **Pure Chrome extension** no server, no Node.js, no npm, no setup beyond loading the extension

---

## New Features (v1.1.0)

### Background Themes
- **Bing Wallpaper** - Daily automatic wallpaper from Bing with navigation to browse recent 8 images
- **Custom Image** - Upload your own image from local files
- **Auto theme extraction** - Automatically detects image colors and applies matching overlay transparency

### Side Panel Mode
- Use Tab Out as a side panel on any webpage
- Right-click extension icon → "Open side panel"
- Auto-refresh when new tabs are created or loaded

### Bilingual Support
- Switch between English and Chinese (中文)
- All UI text fully localized

### Apple-Inspired Design
- Modern, clean interface with glassmorphism effects
- Smooth animations and hover effects
- System font stack (SF Pro on Mac, Segoe UI on Windows)

---

## Background Modes

Tab Out supports three background modes:

1. **None (Default)** - Clean solid color background
2. **Bing Wallpaper** - Daily automatic wallpaper from Bing (click arrows to browse recent 8 images)
3. **Custom Image** - Upload your own image from local files

The extension automatically extracts the dominant color from your background image and applies a subtle overlay to ensure text remains readable.

---

## Side Panel Mode

Tab Out can work as a side panel on any webpage:

1. Right-click the Tab Out extension icon in Chrome
2. Select "Open side panel"
3. Tab Out will appear as a narrow sidebar on the right side of your current page

Features:
- Manual refresh button to update tab list
- Auto-refresh when new tabs are created or pages finish loading
- Optimized layout for narrow sidebar width

---

## Manual Setup

**1. Clone the repo**

```bash
git clone https://github.com/zarazhangrui/tab-out.git
```

**2. Load the Chrome extension**

1. Open Chrome and go to `chrome://extensions`
2. Enable **Developer mode** (top-right toggle)
3. Click **Load unpacked**
4. Navigate to the `extension/` folder inside the cloned repo and select it

**3. Open a new tab**

You'll see Tab Out.

---

## How it works

```
You open a new tab
  -> Tab Out shows your open tabs grouped by domain
  -> Homepages (Gmail, X, etc.) get their own group at the top
  -> Click any tab title to jump to it
  -> Close groups you're done with (swoosh + confetti)
  -> Save tabs for later before closing them
```

Everything runs inside the Chrome extension. No external server, no API calls, no data sent anywhere. Saved tabs are stored in `chrome.storage.local`.

---

## Tech stack

| What | How |
|------|-----|
| Extension | Chrome Manifest V3 |
| Storage | chrome.storage.local |
| Sound | Web Audio API (synthesized, no files) |
| Animations | CSS transitions + JS confetti particles |
| Background | Bing HPImageArchive API + Canvas color extraction |

---

## License

MIT

---

Built by [Zara](https://x.com/zarazhangrui)
