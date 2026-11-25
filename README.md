# SKYNI Sticky Tasks

![SKYNI Sticky Tasks — Your thoughts. Always visible.](assets/brand/github-hero.png)

**Your thoughts. Always visible.** Paper-like notes for quick tasks, available as a Web/PWA app and a Windows desktop beta.

[Open SKYNI Sticky Tasks Web/PWA](https://skyni-sticky.vercel.app/) · [Windows Beta 1 release](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/tag/v0.1.0-beta.1)

![Windows manager with sample notes](assets/screenshots/windows-manager.jpg)

## Web/PWA

Open the app at [skyni-sticky.vercel.app](https://skyni-sticky.vercel.app/). It opens directly to the workspace and stores notes in IndexedDB in the current browser profile.

- Create, edit, complete, and delete stickers and tasks.
- Choose paper colors and switch between Russian and English.
- Export and import notes as JSON.
- Install it as a PWA when your browser offers installation.
- After the first successful online load, the app shell and required resources are cached for offline reload.

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

The [Windows Beta 1 release page](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/tag/v0.1.0-beta.1) provides the Setup installer, Portable executable, instructions, build information, and SHA-256 checksums. The beta provides independent sticky-note windows with separate task lists.

- Choose yellow, pink, and blue paper; move and resize each note.
- Mark tasks complete, edit them, and scroll longer lists.
- Set Always on Top independently for each sticker.
- Keep notes on this Windows PC. No account or cloud synchronization is provided.

### Windows requirements

- 64-bit Windows. Windows 11 was used for the available desktop checks; Windows 10 and managed corporate devices still need user-side verification.
- Microsoft Edge WebView2 Evergreen Runtime. The portable app depends on it. The installer is configured for per-user installation and can bootstrap a missing runtime online; a fully offline installation requires WebView2 to be provisioned already.
- No administrator rights are intended for the per-user installer, but confirm this under your organization’s policy.

The beta executables are unsigned. Windows SmartScreen, Defender, or corporate endpoint controls may warn or block them. Do not bypass organizational security policy.

### Microsoft Defender SmartScreen warning

When launching Setup or Portable, Windows may display **“Windows protected your PC”**. Beta 1 is not Authenticode-signed and may not yet have sufficient SmartScreen reputation. This warning alone does not indicate malware detection, nor does it establish that a file is safe.

1. Download only from the [official release page](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/tag/v0.1.0-beta.1).
2. Compare the downloaded file's SHA-256 with `SHA256SUMS.txt` from the same release. Open PowerShell in your downloads folder:

   ```powershell
   Get-FileHash -LiteralPath ".\SKYNI-Sticky-Tasks-Setup.exe" -Algorithm SHA256
   Get-FileHash -LiteralPath ".\SKYNI-Sticky-Tasks-Portable.exe" -Algorithm SHA256
   ```

   Run the command for the variant you downloaded. Expected SHA-256 values for Beta 1:

   - Setup: `4ee8fb14f627d9601420907dfcf8a650be240a3667eb87c34d6dd1fc521331b1`
   - Portable: `e5a8bb06cbbf1a4932c01759c1805816116af740ee32b3d3df9f16f24a9eb12b`

3. If the hash differs, do not run the file. A matching hash verifies integrity against the published file, not freedom from malware. Scan the file with antivirus software.
4. If you trust the source, have verified the file, and your device policy permits it, select **More info → Run anyway** in SmartScreen if that option is available. If unsure, select **Don't run**.

Do not disable SmartScreen or Defender or circumvent organizational restrictions. If policy blocks execution, contact your administrator or use the [Web/PWA](https://skyni-sticky.vercel.app/). Reputation can differ between builds; disappearance of the warning is not guaranteed.

### Privacy, storage and removal

Web/PWA notes stay in IndexedDB in the browser profile where they were created. Desktop notes stay in the local Windows user profile. Neither version requires an account or provides cloud synchronization. Export important notes as JSON backups. Browser and Desktop storage are separate.

On some Windows 11 systems the app may not appear in **Installed Apps** or **Programs and Features**. The cause has not been established. If the standard list does not show it, use the app’s Settings uninstall action or the Start menu uninstall shortcut where available. Uninstalling with the app-data option disabled preserves notes.

## Screenshots

| Yellow | Pink | Blue |
| --- | --- | --- |
| ![Yellow note](assets/screenshots/windows-sticker-yellow.png) | ![Pink note](assets/screenshots/windows-sticker-pink.png) | ![Blue note](assets/screenshots/windows-sticker-blue.png) |

These screenshots show the real Windows application with demonstration notes.

## FAQ

**Is the Web/PWA app available?** Yes. Open [skyni-sticky.vercel.app](https://skyni-sticky.vercel.app/). It uses local browser storage and has no cross-device sync.

**Where can I download the Windows beta?** The installer, Portable executable, instructions, build information, and SHA-256 checksums are available on the [Windows Beta 1 release page](https://github.com/chistovd4d4-ship-it/SKYNI-Sticky-Tasks-Releases/releases/tag/v0.1.0-beta.1).

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

Ideas, suggestions, or feedback: [info.sticky@familylinck.com](mailto:info.sticky@familylinck.com).

Follow [SKYNI Labs on LinkedIn](https://www.linkedin.com/company/144806007/).

## Language

[Русская версия](README.ru.md)
