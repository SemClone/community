# SEMCL.ONE Community

Community documentation and resources for SEMCL.ONE.

## Structure

```
community/
├── docs/                  # Website files
│   ├── index.html        # Main homepage
│   ├── user_guides/      # User guides and documentation
│   ├── presentations/    # Slide decks and presentations
│   └── examples/         # Practical examples and sample code
└── README.md
```

## Getting Started

### Local Development

Simply open `docs/index.html` in your browser to view the site locally:

```bash
open docs/index.html
```

### Hosting

This is a static site that can be hosted on:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting service

#### GitHub Pages Setup

1. Push this repository to GitHub
2. Go to Settings > Pages
3. Select the branch (usually `main`) and **`/docs` folder**
4. Your site will be available at `https://[username].github.io/community/`

## Adding Content

### User Guides

Add HTML files to the `docs/user_guides/` folder. They will automatically be accessible via `user_guides/your-guide.html`.

### Presentations

Add HTML presentation files to the `docs/presentations/` folder (e.g., reveal.js presentations).

### Examples

Add example files to the `docs/examples/` folder.

## Design

The site follows the SEMCL.ONE design system:
- Primary color: `#9B0002`
- System fonts
- Clean, modular card-based layout
- Responsive design

## Links

- [SEMCL.ONE](https://semcl.one)
- [Status Dashboard](https://status.semcl.one)
