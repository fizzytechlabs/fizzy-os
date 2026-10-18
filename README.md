# FizzyOS 0.1

A browser-based personal desktop with glassy windows, Aero-inspired original CSS wallpaper, and five starter apps. No build tools, package installation, API keys, or backend required.

## Run locally

Open a terminal in this folder and run:

```sh
python3 -m http.server 4173 --directory dist
```

Visit http://localhost:4173. Stop the server with Ctrl+C. You can also open `dist/index.html` directly, but a local server gives consistent browser storage behavior.

## Use the desktop

- Click an application icon once to open it. Dock dots show running apps.
- Drag a window by its title bar; drag its bottom-right corner to resize.
- Red closes, yellow minimizes, green toggles maximization. Double-click a title bar to maximize. The dock restores minimized apps.
- Desktop in the menu bar hides/restores windows. Escape closes the top window.
- On narrow screens, apps fill the available workspace and remain scrollable; the dock switches apps.
- Music plays synthesized ambient chords, with play/pause, seek, volume, previous/next and automatic advancement. Open a local audio file to play your own music. Local files are not uploaded or remembered after a reload. Minimized or closed music windows leave playback running; reopen to pause.
- Terminal is a fixed simulated command set. `help`, `neofetch`, `coffee`, `matrix`, `sudo hire fizzy`, and `cat curiosity.txt` are worth trying. Up/down arrows recall commands. No commands run on your computer.
- Settings stores theme, wallpaper, interface sounds, and reduced-motion preferences in this browser's local storage. Reset restores defaults. Clearing browser data resets preferences.

## Customize

All content is in three small files under `dist/`:

- `index.html`: page title, desktop headline, welcome screen and menu bar.
- `app.js`: edit `renderAbout` for your bio; edit the `projects` array for project names, categories and descriptions, plus `renderPortfolio` to include your real image/video assets; edit `tracks` and the music rendering/playback functions to include permanent audio; edit terminal `responses` for your own easter eggs.
- `style.css`: fonts, colors, window surfaces, icons, layout and three CSS wallpapers. Color tokens at the top control app appearance. `[data-wall]` rules define wallpapers; `[data-theme="dark"]` defines the dark palette.

Place your own images/audio/video under `dist/assets/` and reference them with relative URLs. All portfolio titles, artwork, and biography copy are explicitly starter placeholders. No client work, contact details, or private personal information is included.

Typography uses Google Fonts (DM Sans and Space Grotesk) with local sans-serif fallbacks. The desktop remains functional without those fonts. All wallpaper and sample artwork is CSS; demo audio is synthesized with Web Audio. No external media licenses are needed for these generated shapes and tones.

## Scope

This is a browser desktop, not a real operating system. There is no login database, cloud file storage, private document access, analytics, or shell execution. Window positions and music state are session-only; appearance settings persist locally. Hosted access is owner-private by default.

## Verification

Checked JavaScript syntax and local HTTP serving. Browser checks covered startup, app launching, portfolio filtering/detail navigation, safe terminal response, music play/pause and track switching, and preference persistence after reload. Responsive layouts use a 700px breakpoint, with app scrolling and a persistent dock.
