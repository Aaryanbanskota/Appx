# AppX

**A Play Store–style app store for open-source apps.**

AppX is a mobile-first front-end prototype of an app store where every app is open source. Each app page shows its license, a link to its source code, a security check summary, its permissions and community reviews, so people can see what they are installing before they install it.

> **Status:** prototype. It is built with plain HTML, CSS and JavaScript and has no backend. Downloads, scans and sign-in are simulated.

## Features

- **Familiar store layout:** Home, Games, Apps, Search and Downloads with a bottom navigation bar and a slide-in side menu.
- **Open source first:** every app lists its license (GPL, MIT, Apache, MPL) and has a source code link. Search can filter by license and category.
- **Trust badges:**
  - A ✓ means the app is verified by an admin.
  - A ? means the app is not verified yet.
  - A security section shows a VirusTotal-style scan result, signature check and license.
- **Clear permissions:** each permission has an icon, a plain explanation and a Normal or Sensitive label.
- **Ratings and reviews:** average rating, a bar for each star level, review cards, and a form to post your own review.
- **Download manager:** live progress, pause, resume and cancel, plus a download history and an Update tab.
- **My apps:** open or uninstall installed apps.
- **Settings:** appearance (system, dark or light), download preferences, privacy, repositories, help and about.
- **Light and dark themes**, with hidden scroll bars for a cleaner app feel.

## Pages

| Area | Pages |
| --- | --- |
| Browse | `index.html`, `games.html`, `apps.html`, `search.html`, `categories.html`, `charts.html` |
| App | `app.html?id=0` (details, security, permissions, reviews) |
| Library | `downloads.html`, `myapps.html`, `update.html` |
| Account | `login.html`, `profile.html`, `notifications.html` |
| Settings | `settings.html`, `appearance.html`, `dlprefs.html`, `privacy.html`, `sources.html`, `help.html`, `about.html` |

## Getting started

No build step or dependencies are needed.

```bash
git clone https://github.com/<your-username>/appx.git
cd appx
# open index.html in your browser
```

You can also serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Project structure

```
appx/
├── index.html          # Home
├── ...                 # One HTML file per page
└── assets/
    ├── style.css       # Shared styles and theme tokens
    └── app.js          # Shared data, icons, navigation and helpers
```

App data, icons and shared UI helpers live in `assets/app.js`. To add an app, add an entry to the `A` array. Your login, theme, settings, downloads and reviews are saved in the browser with `localStorage`.

## Roadmap

- Real backend and app catalog
- Real VirusTotal scanning and admin verification workflow
- Developer accounts and app submission
- Screenshot viewer and a wishlist page
- Real source repository links and release downloads

## Contributing

Issues and pull requests are welcome. Please open an issue first to discuss larger changes.

## License

Add your license here, for example MIT.