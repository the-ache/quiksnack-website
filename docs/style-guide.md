# QuikSnack: Fresh Break Style Guide (v1, Sep 2026)

**Name:** always **QuikSnack**: one word, capital Q, capital S. Never "Quik Snack", "Quiksnack", or "QuickSnack".
**Tagline:** *Your breakroom, fully stocked.*
**Feel:** friendly, bright, modern breakroom. Warm and optimistic, with a nod to healthier options.

## 1. Color

### Core palette
| Swatch | Hex | Name | Role |
|---|---|---|---|
| 🟧 | `#FF5A36` | Coral | Primary action color: primary buttons, step 1, logo "Quik", accents. **Fill only, never text on light backgrounds.** |
| 🟦 | `#1F2A44` | Navy | Main text, headings, dark sections, dark buttons, logo "Snack". |
| ⬜ | `#FFF7EC` | Cream | Page background, text on navy. |
| 🟩 | `#2BB673` | Green | "Healthy" cue, success, status dots, step 3. **Fill only.** |
| 🟨 | `#FFC845` | Yellow | Highlight blocks (service-area band), icon tiles, step 2, accent text on navy. |

### Support tints (for text and soft backgrounds)
| Hex | Name | Use |
|---|---|---|
| `#B93A1C` | Coral Deep | Coral-colored **text** (tagline, links), primary-button shadow. |
| `#1B7A48` | Green Deep | Green **text** (eyebrows, "Healthy" tags). |
| `#4A5568` | Ink Muted | Secondary body text on cream or white. |
| `#2A3756` | Navy 2 | Cards and panels inside navy sections. |
| `#C9D1E0` | Mist | Secondary text on navy. |
| `#FFE7DF` | Coral Soft | Option 1 card, FAQ toggles, tags. |
| `#E4F6EC` | Green Soft | Option 2 card, eyebrow pills. |
| `#FFF1C9` | Yellow Soft | Photo placeholders, input focus ring, hero blob. |
| `#FFFFFF` | White | Cards and form fields. |

### Contrast rules (WCAG AA 4.5:1 for all body and UI text)
Measured pairs:

| Pairing | Ratio |
|---|---|
| Navy on Cream | 13.42 |
| Navy on White | 14.26 |
| Ink Muted on White | 7.53 |
| Coral Deep on Cream | 5.36 |
| Green Deep on Green Soft | 4.76 |
| Navy on Coral (buttons) | 4.59 |
| Navy on Yellow | 9.23 |
| Cream on Navy | 13.42 |
| Yellow on Navy | 9.23 |
| Mist on Navy | 9.29 |

- **Don't:** use cream or white text on Coral (2.92–3.10), Green (2.46–2.61), or Yellow (1.45–1.54). Use Navy text on those fills instead.
- **Don't:** use raw Coral or Green as text on cream or white. Use Coral Deep or Green Deep instead.
- An automated check of the homepage mockup found every text node at **≥ 4.59:1**.

## 2. Typography (Google Fonts)
```html
<link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```

| Style | Font | Weight | Size (desktop → mobile) | Line height | Notes |
|---|---|---|---|---|---|
| H1 | Fredoka | 700 | 64 → 38px (`clamp(2.4rem, 5.2vw, 4rem)`) | 1.1 | Sentence case, `text-wrap: balance` |
| Tagline | Fredoka | 600 | 30 → 22px | 1.1 | Coral Deep |
| H2 | Fredoka | 700 | 44 → 30px | 1.1 | Sentence case |
| H3 / card titles | Fredoka | 600 | 22px | 1.1 | |
| Lede | Inter | 400 | 18.4px | 1.6 | Ink Muted |
| Body | Inter | 400 | 17 → 16px | 1.6 | Navy or Ink Muted |
| Eyebrow | Inter | 600 | 13.6px, uppercase, +0.04em | 1.2 | Green Deep on Green Soft pill |
| Label / small | Inter | 600 / 500 | 14–15px | 1.4 | |
| Buttons | Fredoka | 600 | 17px (16px small) | 1 | |

- Headings are **sentence case**. The old site's all-caps headings are gone.
- Fallback stacks: `'Fredoka', 'Trebuchet MS', system-ui, sans-serif` and `'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif`.

## 3. Buttons
All buttons share these specs:
- Pill shape (`border-radius: 999px`)
- Fredoka 600 17px
- Padding 16px × 26px
- Hover: lift 2px
- Focus: 3px Navy outline, 3px offset
- Full width on mobile

| Variant | Fill | Text | Border / effect | Hover | Use |
|---|---|---|---|---|---|
| **Primary** | Coral `#FF5A36` | Navy | 6px Coral Deep bottom shadow ("snack-button" depth) | `#FF7A5C` | One main action per view: "Get a machine for your office", "Get a machine", "Request a machine" |
| **Secondary** | Transparent | Navy | 2px Navy border | Navy fill, Cream text | Paired action: "Text Scott" |
| **Dark** | Navy | Cream | none | `#2A3756` | Actions on soft or colored panels: "Ask about Option 1/2", "Text Scott" on the yellow band |
| Small (header) | Coral | Navy | 4px Coral Deep shadow | as Primary | Header "Get a machine" |

**Link text:** Coral Deep, underline offset 3px, hover Navy.

## 4. Shape, spacing, and components
- **Radius:**
  - 20px for cards
  - 24px for big panels (options, contact)
  - 12px for inputs
  - 999px for pills and buttons
- **Shadow:** `0 10px 30px rgba(31,42,68,.10)` on white cards.
- **Layout:**
  - Max content width 1180px, 24px side padding.
  - Section padding is 96px vertically (64px on mobile).
  - Breakpoints at 980px (two columns become one) and 760px (mobile nav, stacked cards).
- **Step numbers:** 52px rounded squares filled Coral, Yellow, then Green, with a Navy numeral.
- **Photo placeholders:** yellow striped block with a dashed Navy border and a camera icon. The label reads "Photo: …". Use **real photos only** (installed machines, real snacks, real breakrooms), never AI images of fake products.
- **Cookie notice:** small white toast in the bottom-left corner, max 340px wide, one line of text and an "OK" button. Never a full-width or colored banner.

## 5. Logo usage (recommended: Concept A, "Happy Vendy")
**Files:** `assets/` (repo root)
- `A-happy-vendy-lockup.svg` / `.png`: primary horizontal lockup, for light backgrounds.
- `A-happy-vendy-lockup-reverse.svg` / `.png`: for Navy backgrounds. The icon body switches to Cream and "Snack" to Cream.
- `A-happy-vendy-icon.svg` / `.png`: the icon mark alone (a friendly vending machine with coral, yellow, and green snack rows and a coral smile).
- Favicon set: the repo root, containing:
  - `favicon.svg` (simplified icon)
  - `favicon.ico` (16/32/48)
  - `favicon-16.png`, `favicon-32.png`, `favicon-48.png`
  - `apple-touch-icon.png` (180, on Cream)
  - `icon-512.png`

**Rules:**
- **Clear space:** at least the width of the icon's window (about ¼ of the icon height) on every side.
- **Minimum size:**
  - Lockup: 32px tall on screen (about 120px wide) or 25mm wide in print.
  - Icon: 24px (use the favicon version below 32px).
- **Backgrounds:**
  - Use the primary lockup on Cream or White.
  - Use the reverse lockup on Navy.
  - Don't place the full-color lockup on Coral, Green, or Yellow. Put it on a Cream panel instead. A one-color Navy version is a to-do.
- **Colors:** "Quik" is Coral and "Snack" is Navy (Cream in the reverse). Don't swap, recolor, or add gradients.
- **Don't:**
  - Stretch, rotate, outline, or shadow the logo.
  - Retype the wordmark in another font. The wordmark is Fredoka 700 outlines, so use the files.
  - Separate "Quik" and "Snack" with a space.
- **Accessibility note:** the Coral "Quik" is 2.9:1 on Cream. That's acceptable for a logotype (WCAG exempts logos), but it's why Coral is never used for body text.
- **Alternates kept on file:** Concept B "Bite & Go" and Concept C "Sticker Pop". Sticker Pop's badge suits merch, stickers, and machine decals.

## 6. Voice and copy
- **Tone:** friendly, short, and local, with plain-English benefits.
  - Say: "You pick the snacks. We bring the machine and keep it full."
  - Avoid: "Able to Provide Healthy & Indulgent Snacks."
- **Always state who pays:**
  - **Option 1:** people pay at the machine.
  - **Option 2:** company benefit, with the business billed on one monthly invoice.
- **Key facts to reuse:**
  - Locally owned & operated
  - Healthy and indulgent snacks
  - Apple Pay, Google Pay, cards, cash, and coins
  - Serving Huntsville and Madison, AL
  - Scott: 256-509-5670 (call or text), scott@quiksnack.com
