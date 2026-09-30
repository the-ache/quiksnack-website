# QuikSnack website

Homepage for **QuikSnack**: vending machine placement, stocking, and remote monitoring for workplaces in Huntsville and Madison, Alabama. This is the "Fresh Break" rebrand (coral, navy, cream, green, and yellow, set in Fredoka and Inter).

- **Live preview:** https://the-ache.github.io/quiksnack-website/ (GitHub Pages)
- **Brand rules:** [docs/style-guide.md](docs/style-guide.md)

## What's here
| Path | What it is |
|---|---|
| `index.html` | The whole homepage in one file: HTML plus inline CSS. Fonts load from Google Fonts. |
| `favicon.*`, `favicon-*.png`, `apple-touch-icon.png`, `icon-512.png` | Browser, phone, and app icons |
| `assets/` | Logo files (SVG and PNG). Concept A, "Happy Vendy", is the one the site uses. B and C are alternates. |
| `docs/style-guide.md` | Colors, type, buttons, and logo usage |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is |

## How to edit
1. Open `index.html` in any text editor.
   - The copy is plain HTML, grouped into commented sections (HERO, HOW IT WORKS, OPTIONS, PROOF POINTS, FAQ, CONTACT).
   - Colors and fonts are CSS variables at the top of the `<style>` block (`--coral`, `--navy`, and so on).
2. Replace the striped "Photo: …" placeholder blocks with real photos. Put the images in `assets/` and use relative paths such as `assets/machine.jpg`, with no leading `/`, so the page works on both the Pages project URL and a custom domain.
3. To preview locally, open `index.html` in a browser, or run `python3 -m http.server` and visit http://localhost:8000.
4. Commit and push to `main`. GitHub Pages redeploys automatically in about a minute.

## Not done yet
- **The contact form is not hooked up.** It's a placeholder, and submitting it only shows a message on the page. Before launch, connect it to a form service (for example Formspree or Netlify Forms) or a small backend. The phone, text, and email links do work.
- **No custom domain yet.** There is no `CNAME` file, and quiksnack.com's DNS still points at the old GoDaddy site.
- The photo placeholders need real photos of QuikSnack machines.

© 2026 QuikSnack
