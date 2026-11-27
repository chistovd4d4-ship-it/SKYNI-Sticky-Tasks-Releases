# SKYNI Sticky Tasks

![SKYNI Sticky Tasks — Your thoughts. Always visible.](assets/brand/github-hero.png)

**Your thoughts. Always visible.** Paper-like notes for quick tasks, available as a Web/PWA app and a Windows desktop beta.

[Open SKYNI Sticky Tasks Web/PWA](https://skyni-sticky.vercel.app/) · [Windows Beta 3 release](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/tag/v0.2.0-beta.3)

![Windows manager with sample notes](assets/screenshots/windows-manager.jpg)

## Web/PWA

Open the app at [skyni-sticky.vercel.app](https://skyni-sticky.vercel.app/). It opens directly to the workspace and stores notes in IndexedDB in the current browser profile.

- Create, edit, complete, and delete stickers and tasks.
- Choose paper colors and switch between Russian and English.
- Export and import notes as JSON.
- Install it as a PWA when your browser offers installation.
- After the first successful online load, the app shell and required resources are cached for offline reload.

### Web v1.4.0

- Reorder tasks inside a sticker by drag and drop, keyboard controls, or the task menu; task order is preserved through reload and JSON export/import.
- Due dates follow the local calendar: tasks due in 1–4 days are amber, and tasks due today or earlier are red when unfinished.
- Manage recovery backups in Settings next to JSON export/import. The app creates a verified local backup before import replaces workspace data; valid backups show their creation time and can be downloaded or restored after confirmation.
- Settings uses a thin, rounded scrollbar styled for Light/Dark/System. Native wheel, touch, and keyboard scrolling remain available.
- Existing local storage, attachments, offline/PWA update behavior, and detached sticker windows remain supported.

### Web v1.3.1

- Hovering a resize edge or corner shows one branded directional indicator without a duplicate system resize cursor. Resize behavior and hit areas remain unchanged.

### Web v1.3.0

- Resize Web stickers from all eight edges and corners. Their sizes and board positions persist locally and remain unchanged when the browser window is temporarily resized.
- Set a local due date on a task; overdue unfinished tasks are shown in red.
- Choose yellow, cream, pink, blue, or green paper. Long task text that does not fit shows a full wrapped tooltip after a short delay, including in a detached sticker window.
- Distinguish web links and email attachments with Globe and Mail icons. Existing task markers, `.msg`/`.eml` attachments, and URL attachments remain available.
- Switch RU/EN and Light/Dark/System. Task content stays in this browser profile; Web v1.2.0 IndexedDB data and JSON backups remain supported.

![SKYNI Sticky Tasks Web v1.3.0 workspace](assets/screenshots/web-v1.3.0-workspace.png)

Browser notes are separate from Windows Desktop notes. Neither version synchronizes notes between devices. A regular browser popup cannot guarantee Always on Top; Document Picture-in-Picture is available only in supported browsers and contexts.

### Install the PWA

1. Open [the Web app](https://skyni-sticky.vercel.app/) and let it finish loading once while online.
2. In a supported browser, choose **Install app** from the address-bar install control or browser menu. On mobile, use **Add to Home Screen** if your browser offers it.
3. Open the installed app from your applications list or home screen. Offline startup is available after the initial successful load.

Install controls vary by browser and device. The web app remains usable in a normal browser tab when installation is not offered.

### Task markers and attachments (Web v1.2.0)

- Add, change, or remove five translucent task-row markers: red, yellow, green, blue, and purple.
- Attach one HTTP/HTTPS or webmail link, or one `.msg` / `.eml` file to a task. Email files are limited to 20 MB each.
- Email files are stored in IndexedDB in the current browser profile. They are not uploaded to SKYNI servers and are excluded from analytics. JSON export/import includes the attachments.
- Links open in a new browser tab. Browsers may download `.msg` / `.eml` files for the installed mail app; automatic Outlook launch and direct Outlook drag-and-drop depend on browser support.

## Windows desktop beta

Windows 0.2.0-beta.3 is the current privacy-remediated prerelease: [Setup](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/download/v0.2.0-beta.3/SKYNI-Sticky-Tasks-Setup.exe) · [Portable](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/download/v0.2.0-beta.3/SKYNI-Sticky-Tasks-Portable.exe) · [all release files and notes](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/tag/v0.2.0-beta.3).

Beta 1 and Beta 2 have been withdrawn after a privacy review. Their release assets are no longer available; do not install or redistribute previously downloaded copies. Windows Beta 3 is the current privacy-remediated prerelease.

Beta 2 adds task reordering by drag and drop or keyboard controls, amber upcoming-deadline and red overdue highlighting, five task color markers, green sticky notes, URL and email-file attachments, resizable independent windows, export/import, and verified local backups. The Web and Windows versions keep separate local data; there is no account or cloud sync.

### Upgrade from Beta 1

Beta 1 does not include an updater. The first transition is manual. Close Beta 1 and make and verify an external backup of the complete application data folder (workspace, settings, geometry, backups, and attachments). Beta 1 has been withdrawn; rollback to it is not recommended. Download [Beta 3 Setup](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/download/v0.2.0-beta.3/SKYNI-Sticky-Tasks-Setup.exe), verify it against the release signatures and `SHA256SUMS.txt`, then install manually. Keep the existing application data directory and verify your notes after the first launch. Do not remove the backup until migration is confirmed.

### Windows requirements and signature status

- 64-bit Windows and Microsoft Edge WebView2 Evergreen Runtime. The installer can download a missing runtime; Portable requires WebView2 to be present.
- Setup has a Tauri updater signature and a Minisign signature; Portable has a Minisign signature. SHA-256 checksums are published for the release files. They are **not Authenticode-signed**; SmartScreen or endpoint protection may warn. Do not bypass organizational security policy.
- The built-in production update manifest is intentionally not activated yet. The current endpoint has no manifest, so Beta 2 is not offered in-app. Real updater installation and rollback have not been tested.

### Known limitations

- EML/MSG handling and direct Outlook drag-and-drop were not tested in the manual acceptance; they were conditionally accepted for this beta.
- Real updater installation, restart, and rollback remain untested in an isolated Windows VM/Sandbox.
- Windows 10, managed devices, unusual DPI and multi-monitor combinations still need additional device acceptance.

### Privacy, storage and removal

Web/PWA notes stay in IndexedDB in the browser profile where they were created. Desktop notes stay in the local Windows user profile. Neither version requires an account or provides cloud synchronization. Export important notes as JSON backups. Browser and Desktop storage are separate.

On the Production Web site, Vercel Analytics measures canonical page views only. It does not receive sticker or task text, local IDs, query parameters, or attachment contents. Core app features and local storage continue to work when analytics is unavailable.

On some Windows 11 systems the app may not appear in **Installed Apps** or **Programs and Features**. The cause has not been established. If the standard list does not show it, use the app’s Settings uninstall action or the Start menu uninstall shortcut where available. Uninstalling with the app-data option disabled preserves notes.

## Screenshots

| Yellow | Pink | Blue |
| --- | --- | --- |
| ![Yellow note](assets/screenshots/windows-sticker-yellow.png) | ![Pink note](assets/screenshots/windows-sticker-pink.png) | ![Blue note](assets/screenshots/windows-sticker-blue.png) |

These screenshots show the real Windows application with demonstration notes.

## FAQ

**Is the Web/PWA app available?** Yes. Open [skyni-sticky.vercel.app](https://skyni-sticky.vercel.app/). It uses local browser storage and has no cross-device sync.

**Where can I download the Windows beta?** Download [Windows Beta 3 Setup](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/download/v0.2.0-beta.3/SKYNI-Sticky-Tasks-Setup.exe), [Portable](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/download/v0.2.0-beta.3/SKYNI-Sticky-Tasks-Portable.exe), and the full [release package](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/tag/v0.2.0-beta.3). Beta 1 and Beta 2 assets have been withdrawn and are unavailable. Do not install or redistribute previously downloaded copies. The production updater manifest is not active yet.

**Will notes sync between Web and Windows?** No. Each version uses its own local storage.

**Does Portable mean fully self-contained?** No. The Windows executable requires WebView2 Evergreen Runtime.

**Will a web sticker always stay above every application?** A regular browser popup cannot promise this. Document Picture-in-Picture depends on browser support and system restrictions.

## Known limitations

- Windows 10, corporate-managed PCs, multi-monitor/DPI combinations, and missing-runtime installation need additional target-device acceptance.
- Unsigned Windows executables can trigger security warnings.
- Some Windows 11 configurations may omit the app from standard installed-app lists; use the in-app Settings action or Start menu uninstall shortcut.
- Web/PWA installation depends on browser and device support; offline use requires an initial successful online load.
- No macOS or iOS desktop package is available.

## Feedback

Ideas, suggestions, or feedback: [open a GitHub issue](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/issues).

Follow [SKYNI Labs on LinkedIn](https://www.linkedin.com/company/144806007/).

## Language

[Русская версия](README.ru.md)
