# QuikSnack website

Homepage for **QuikSnack**: vending machine placement and restocking for workplaces in Huntsville and Madison, Alabama. This is the "Fresh Break" rebrand (coral, navy, cream, green, and yellow, set in Fredoka and Inter).

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

## Contact form
The form is connected to **Formspree** (form ID `xjykljbb`, endpoint `https://formspree.io/f/xjykljbb`). Submissions are emailed to **scott@quiksnack.com**.
- Fields: `name`* and `email`* (required), plus `phone`, `company`, `location`, `option`, and `message`. The subject line is set by a hidden `_subject` field ("New QuikSnack website inquiry"). Because the email field is named `email`, Formspree sets it as the reply-to.
- Spam protection: a hidden honeypot field named `_gotcha`. Submissions that fill it in are dropped.
- With JavaScript, the page submits the form in the background and shows a thank-you message in place, or an error with the phone number and email. Without JavaScript, it posts normally to Formspree's own thank-you page.
- To change where submissions go, or to see past submissions, log in to Formspree. The page doesn't need to change.

## Not done yet
- **No custom domain yet.** There is no `CNAME` file, and quiksnack.com's DNS still points at the old GoDaddy site.
- The hero and gallery use illustrations. Swap in real photos of QuikSnack machines when they're available.

© 2026 QuikSnack
