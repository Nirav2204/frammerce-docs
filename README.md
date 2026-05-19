# Frammerce Docs

The user guide + component reference for the Frammerce Framer plugin, built with [Mintlify](https://mintlify.com/).

## Run locally

```bash
npm install
npm run dev
```

Mintlify dev server boots at `http://localhost:3000` (default). The first start takes ~30s while it downloads the preview engine; subsequent runs are instant.

## Structure

```
docs/
├── docs.json                 # Mintlify config (navigation, branding, links)
├── favicon.svg               # Browser tab icon
├── logo/                     # Header logos (light + dark)
├── images/                   # Drop screenshots here (referenced as /images/...)
│
├── introduction.mdx          # Landing page
├── quickstart.mdx            # 5-minute setup walkthrough
├── get-shopify-token.mdx     # How to generate a Storefront API token
│
├── cms-sync.mdx              # Syncing products to Framer CMS
├── sync-settings.mdx         # The 4 sync-settings toggles
├── cart-runtime.mdx          # How the shared cart runtime works
├── publishing.mdx            # What ships when you Publish
├── plans-and-licenses.mdx    # Tiers, comparison, license activation
├── settings.mdx              # Plugin Settings page
├── troubleshooting.mdx       # Common issues and fixes
├── faq.mdx                   # General questions
│
└── components/
    ├── overview.mdx          # All 21 components, grouped
    ├── product/              # 7 product components
    │   ├── product-gallery.mdx
    │   ├── product-price.mdx
    │   ├── variant-picker.mdx
    │   ├── quantity-input.mdx
    │   ├── stock-status.mdx
    │   ├── add-to-cart.mdx
    │   └── buy-now.mdx
    └── cart/                 # 14 cart components
        ├── cart-button.mdx
        ├── item-count-badge.mdx
        ├── cart-close-button.mdx
        ├── cart-item-list.mdx
        ├── cart-item-row.mdx
        ├── line-image.mdx
        ├── line-title.mdx
        ├── line-variant-info.mdx
        ├── line-quantity-stepper.mdx
        ├── line-unit-price.mdx
        ├── line-total-price.mdx
        ├── remove-button.mdx
        ├── cart-subtotal.mdx
        └── checkout-button.mdx
```

## Adding screenshots

Drop PNG/JPG files into `images/` and reference them in MDX as `/images/your-file.png`. Suggested screenshots:

- `images/hero-light.png` / `hero-dark.png` - introduction hero (1200x630)
- `images/quickstart-connect.png` - plugin connect form
- `images/cms-page.png` - CMS sync screen
- `images/sync-settings.png` - sync settings page
- `images/settings-page.png` - settings page

## Editing content

Each `.mdx` file has frontmatter (`title`, `description`) at the top and Markdown + MDX components below. Common components used:

- `<Card>`, `<CardGroup cols={2}>` - linkable cards
- `<Steps>` + `<Step title="...">` - numbered walkthroughs
- `<Note>`, `<Warning>`, `<Tip>` - callouts
- `<AccordionGroup>` + `<Accordion title="...">` - expandable sections

Reference: https://mintlify.com/docs/

## Useful commands

```bash
npm run dev            # Local preview with hot reload
npm run broken-links   # Validate all internal links
npm run rename         # Rename a page and update references
```

## Publishing

To publish docs to a live URL (e.g. `docs.frammerce.dev`):

1. Sign up at [mintlify.com](https://mintlify.com/) and create a new docs site
2. Connect this repo (or push the `docs/` folder to its own repo)
3. Mintlify deploys on every push to `main`

See https://mintlify.com/docs/quickstart for the full publish flow.
