# Papyra / ورقتي — public site

Static privacy, support, and terms site for the **Papyra** (English) / **ورقتي** (Arabic)
document-scanner app for iPhone and iPad. Plain HTML + CSS, no build step — designed to be
served directly by **GitHub Pages** from the repository root.

## Structure

```
/
├── index.html              Landing (English-primary, bilingual brand)
├── privacy/index.html      Privacy Policy (EN)
├── support/index.html      Support & FAQ (EN)
├── terms/index.html        Terms of Use (EN)
├── ar/
│   ├── index.html          Landing (Arabic, RTL)
│   ├── privacy/index.html  Privacy Policy (AR, RTL)
│   ├── support/index.html  Support & FAQ (AR, RTL)
│   └── terms/index.html    Terms of Use (AR, RTL)
├── assets/
│   ├── styles.css          Shared stylesheet (light/dark, LTR/RTL via logical properties)
│   └── favicon.svg         Placeholder brand mark — replace with the final app glyph
├── .nojekyll               Serve files as-is (no Jekyll processing)
└── README.md
```

Every page cross-links to its counterpart in the other language, and links between pages are
**relative**, so the site works under any domain (e.g. `papyra.app` or
`<user>.github.io/papyra-site`) without edits.

## Publishing (GitHub Pages)

1. Create a public repository and push these files to its default branch.
2. In **Settings → Pages**, set the source to that branch, folder `/` (root).
3. The site's URLs then map directly to the structure above (e.g. `/privacy/`, `/ar/support/`).

The App Store Connect fields map as:

- **Privacy Policy URL** → `/privacy/` (and `/ar/privacy/` for the Arabic listing)
- **Support URL** → `/support/` (and `/ar/support/`)
- **Terms of Use (EULA) URL** → `/terms/` (and `/ar/terms/`)

## Notes

- Contact email throughout is **hamam@gccapps.com**.
- The privacy policy reflects the app's actual behaviour: strictly local-only, no servers,
  no analytics, no tracking. It must stay in sync with the store privacy declarations in the
  app repo at `docs/release/APP_PRIVACY_DECLARATIONS.md`.
- Replace `assets/favicon.svg` with the final app icon glyph once available.
