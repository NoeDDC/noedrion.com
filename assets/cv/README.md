The site's "Download CV" button links to the PDF matching the current
language toggle: `assets/cv/Noe-Drion-CV-FR.pdf` in French,
`assets/cv/Noe-Drion-CV-EN.pdf` in English (see the two `lang-fr`/`lang-en`
links in the hero section of `index.html`).

`source-fr.html` and `source-en.html` are the editable sources of those PDFs
(single-column, ATS-friendly layout, matching the site's fonts/accent
colors). Keep both in sync when updating content. To regenerate a PDF:

```
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --disable-gpu --no-pdf-header-footer \
  --print-to-pdf="Noe-Drion-CV-FR.pdf" --print-to-pdf-no-header \
  "$(pwd)/source-fr.html"
```

(swap `-FR`/`fr` for `-EN`/`en` for the English version.)
