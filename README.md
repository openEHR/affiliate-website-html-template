# openEHR Affiliate Website Template

A simple, modern single-page website template for openEHR affiliates. No frameworks, no build process - just clean HTML, CSS, and placeholders ready to be customized.

## Features

- Single-page design (no scrolling required initially)
- Clean, modern appearance inspired by openEHR.lu and openEHR.ch
- Uses Soehne Breit font (official openEHR typography)
- Official openEHR logos and branding
- Responsive layout (works on mobile, tablet, desktop)
- Prominent link to your Discourse discussion area
- Plain HTML/CSS (no React, no templating engines, no build tools)

## Quick Start

1. Open `index.html` in VS Code
2. Use Find & Replace (Ctrl+H or Cmd+H) to replace the placeholders:

### Required Placeholders

| Placeholder | Example | Description |
|------------|---------|-------------|
| `COUNTRY_NAME` | `Netherlands` | Full country name |
| `COUNTRY_CODE` | `netherlands` | Lowercase, used in Discourse URL |
| `AFFILIATE_DESCRIPTION` | `The Dutch openEHR community promoting open health data standards` | Brief meta description |
| `AFFILIATE_TAGLINE` | `Advancing open health data standards in the Netherlands` | Displayed under header |
| `AFFILIATE_INTRO_TEXT` | `We are a community of healthcare professionals, IT specialists...` | Main intro paragraph |
| `CONTACT_EMAIL` | `info@openehr.nl` | Your contact email |
| `ABOUT_US_TEXT` | `openEHR Netherlands is a non-profit organization...` | About section text |
| `GET_INVOLVED_TEXT` | `Join our community discussions, attend our events...` | Getting involved text |

### Optional: Update GitHub Link

The footer includes a "View source on GitHub" link. Update this to point to your affiliate's website repository:

1. Find the comment in the footer: `<!-- TODO: Change this URL to your affiliate's website source code repository -->`
2. Replace the URL with your repository (e.g., `https://github.com/YOUR_ORG/openehr-COUNTRY_CODE-website`)

If you prefer not to display the source link, simply remove the entire `<p class="source-link">` element.

### How to Replace Placeholders in VS Code

1. Open `index.html` in VS Code
2. Press `Ctrl+H` (Windows/Linux) or `Cmd+H` (Mac) to open Find & Replace
3. Enter a placeholder in "Find" (e.g., `COUNTRY_NAME`)
4. Enter your value in "Replace" (e.g., `Netherlands`)
5. Click "Replace All" or use `Ctrl+Alt+Enter` (Windows/Linux) or `Cmd+Option+Enter` (Mac)
6. Repeat for each placeholder

**Tip:** Replace `COUNTRY_CODE` first, as it appears in multiple places including the Discourse URL.

## Discourse Forum Link

Each affiliate has a discussion area on the openEHR Discourse forum following this pattern:

`https://discourse.openehr.org/c/openehr-affiliates/openehr-COUNTRY_CODE`

Examples:
- Netherlands: https://discourse.openehr.org/c/openehr-affiliates/openehr-netherlands
- Switzerland: https://discourse.openehr.org/c/openehr-affiliates/openehr-switzerland

Replace `COUNTRY_CODE` in `index.html` with your country code (lowercase, hyphenated if needed).

## Customization

### Colors

Edit `styles.css` at the top to change colors:

```css
:root {
    --primary-color: #00acbc;     /* Main brand color */
    --secondary-color: #f7a102;   /* Accent color */
    --text-color: #333;           /* Main text */
    --text-light: #666;           /* Lighter text */
}
```

### Logo

The template includes official openEHR logos in the `assets/icons/` folder:
- `logo.svg` - Main logo (used in header)
- `icon.svg` - Favicon icon
- `openehr_logo-square.png` - Square PNG logo (alternate favicon)
- `openehr_logo.png` - Standard PNG logo (fallback)

To use a custom affiliate logo:

1. Add your logo file (e.g., `custom-logo.svg`) to the `assets/icons/` folder
2. In `index.html`, replace:
   ```html
   <img src="assets/icons/logo.svg" alt="openEHR logo" class="logo">
   ```
   with:
   ```html
   <img src="assets/icons/custom-logo.svg" alt="openEHR COUNTRY_NAME logo" class="logo">
   ```

### Font

The template uses **Soehne Breit**, the official openEHR font family, loaded from the Django legacy site. This ensures brand consistency across all openEHR affiliate sites. The font is loaded automatically via CSS - no additional setup required.

## File Structure

```
├── index.html          # Main HTML file with placeholders
├── styles.css          # All styling (modern, responsive)
├── assets/
│   └── icons/          # Official openEHR logos and icons
│       ├── logo.svg                # Main logo (used in header)
│       ├── icon.svg                # Favicon icon
│       ├── openehr_logo-square.png # Square PNG (alternate favicon)
│       └── openehr_logo.png        # Standard PNG (fallback)
└── README.md           # This file
```

## Publishing

1. Upload all files (`index.html`, `styles.css`, and `assets/` folder) to your web hosting
2. Point your domain to the hosting location
3. Done!

## Alternative: Discourse Page Publishing

Instead of a standalone website, affiliates can publish directly on the openEHR Discourse forum:

- https://discourse.openehr.org/t/example-affiliate-page-publishing/11384

This template is for affiliates who prefer a traditional website presence.

## Design Inspiration

This template was inspired by these existing affiliate sites:

- https://openehr.lu/ (clean, modern, single-page)
- https://openehr.ch/ (professional, well-organized)
- https://openehr.no/
- https://openehr.nl/

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## License

This template is provided by the openEHR Foundation for use by official openEHR affiliates.
