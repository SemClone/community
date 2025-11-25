# SEMCL.ONE Community Site - Jekyll Guide

This site has been converted to use Jekyll, a static site generator that's natively supported by GitHub Pages. This means you can now manage content using markdown files and data files, and GitHub will automatically build the site when you push changes.

## 📁 Project Structure

```
community/
├── _config.yml                 # Jekyll configuration
├── _layouts/                   # Page templates
│   ├── default.html           # Base layout with navbar/footer
│   ├── page.html              # Layout for content pages
│   └── article.html           # Layout for individual guides/examples
├── _includes/                  # Reusable components
│   ├── navbar.html            # Site navigation
│   ├── footer.html            # Site footer
│   ├── breadcrumb.html        # Breadcrumb navigation
│   └── back_button.html       # Back to home button
├── _data/                      # Content data files
│   ├── home_components.yml    # Home page component cards
│   ├── presentations.yml      # Presentations content
│   ├── user_guides.yml        # Static user guides links
│   └── examples.yml           # Static examples links
├── _examples/                  # Example articles (collections)
│   ├── getting-started.md
│   └── advanced-scanning.md
├── _user_guides/              # User guide articles (collections)
│   ├── mcp-configuration.md
│   └── understanding-copycatm.md
├── assets/
│   └── css/
│       └── main.css           # Site-wide styles
└── docs/                       # Public pages
    ├── index.html             # Home page
    ├── user_guides/
    │   └── index.html         # User guides listing
    ├── presentations/
    │   └── index.html         # Presentations listing
    └── examples/
        └── index.html         # Examples listing
```

## ✍️ Adding Content

### Adding a New Example (Blog-style)

1. Create a new markdown file in `_examples/`:

```bash
touch _examples/my-new-example.md
```

2. Add frontmatter and content:

```markdown
---
title: My New Example
description: A brief description of this example
date: 2025-01-25
author: Your Name
tags: [tag1, tag2, tag3]
---

# My New Example

Your content here in markdown format...

## Section 1

More content...
```

3. Commit and push - the example will automatically appear on the Examples page!

### Adding a New User Guide (Blog-style)

Same process as examples, but create the file in `_user_guides/`:

```bash
touch _user_guides/my-guide.md
```

```markdown
---
title: My Comprehensive Guide
description: Learn how to do something amazing
date: 2025-01-25
author: Your Name
tags: [guide, tutorial, advanced]
---

# My Comprehensive Guide

Your guide content here...
```

### Adding External Links (Presentations, Static Links)

Edit the YAML data files in `_data/`:

**For presentations** (`_data/presentations.yml`):

```yaml
sections:
  - title: Marketing Materials
    status: available  # or development
    items:
      - title: Introduction to MCP-SEMCLONE
        url: "https://slides.com/your-presentation"  # External link
        description: A user guide on using AI-driven OSS compliance tooling.

      - title: Another Presentation
        url: "/docs/presentations/my-presentation.pdf"  # Local PDF
        description: Description here.
```

**For user guides** (`_data/user_guides.yml`):

```yaml
sections:
  - title: MCP Configuration Options
    status: available
    items:
      - title: External Guide
        url: "https://external-site.com/guide"
        description: Link to external documentation.
```

## 🎨 Customizing the Site

### Updating Site Configuration

Edit `_config.yml` to change:

- Site title and description
- Navigation menu items
- Footer text and links
- Logo URL

```yaml
# Site settings
title: SEMCL.ONE Community
description: Your description here

# Navigation
navigation:
  - title: Home
    url: https://semcl.one/
  - title: GitHub
    url: https://github.com/SemClone/
    external: true
```

### Modifying Home Page Cards

Edit `_data/home_components.yml`:

```yaml
- name: Your New Section
  description: Description of this section
  url: path/to/section/
  button_text: View Section →
  show_progress: true
  progress: 50  # 0-100
```

### Styling Changes

All CSS is in `assets/css/main.css`. The site uses CSS variables for consistent theming:

```css
:root {
    --primary: #9B0002;
    --primary-dark: #7A0001;
    --gray: #666666;
    /* ... */
}
```

## 🚀 Local Development

### Option 1: Using Jekyll Locally (Recommended)

1. Install Ruby and Jekyll:

```bash
gem install jekyll bundler
```

2. Create a `Gemfile` in the project root:

```ruby
source "https://rubygems.org"
gem "jekyll", "~> 4.3"
gem "webrick", "~> 1.8"
```

3. Install dependencies:

```bash
bundle install
```

4. Run the development server:

```bash
bundle exec jekyll serve
```

5. Visit `http://localhost:4000/docs/` in your browser

### Option 2: Without Jekyll (Limited)

Open the HTML files directly in your browser, but note:
- Jekyll variables won't work
- Collections won't be processed
- You won't see the final result

## 📤 Deployment

### GitHub Pages (Automatic)

Just push to your repository! GitHub Pages will automatically:

1. Detect the Jekyll site
2. Build it using Jekyll
3. Deploy to your GitHub Pages URL

No configuration needed - it just works!

### Manual Deployment

If you want to build locally and deploy the static files:

```bash
bundle exec jekyll build
# Upload the _site/ directory to your hosting
```

## 📝 Markdown Features

Your markdown files support:

### Headings

```markdown
# H1
## H2
### H3
```

### Code Blocks

```markdown
\`\`\`bash
npm install -g mcp-semclone
\`\`\`
```

### Lists

```markdown
- Item 1
- Item 2
  - Nested item

1. Numbered item
2. Another numbered item
```

### Links and Images

```markdown
[Link text](https://example.com)
![Alt text](/path/to/image.png)
```

### Tables

```markdown
| Column 1 | Column 2 |
|----------|----------|
| Data 1   | Data 2   |
```

### Blockquotes

```markdown
> This is a quote
```

## 🔧 Advanced Features

### Custom Layouts

Create custom layouts in `_layouts/` for special page types.

### Custom Includes

Add reusable components in `_includes/`:

```html
<!-- _includes/my_component.html -->
<div class="my-component">
  {{ include.content }}
</div>
```

Use it in your pages:

```liquid
{% include my_component.html content="Hello!" %}
```

### Collections

Define new collections in `_config.yml`:

```yaml
collections:
  tutorials:
    output: true
    permalink: /docs/tutorials/:name/
```

Then add default values:

```yaml
defaults:
  - scope:
      type: "tutorials"
    values:
      layout: "article"
```

## 🐛 Troubleshooting

### Site not updating on GitHub Pages?

1. Check GitHub Actions tab for build errors
2. Ensure `_config.yml` is valid YAML
3. Check that file names don't have special characters
4. Wait a few minutes - GitHub Pages can take time to update

### Local development issues?

1. Run `bundle exec jekyll clean` to clear cache
2. Check for YAML syntax errors in frontmatter
3. Ensure all files are UTF-8 encoded

### Links not working?

- Use `{{ site.baseurl }}` for relative links if you have a baseurl set
- Use `| relative_url` filter: `{{ "/docs/" | relative_url }}`

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Liquid Template Language](https://shopify.github.io/liquid/)
- [YAML Syntax](https://yaml.org/spec/1.2/spec.html)

## 💡 Quick Tips

1. **Commit often**: Each push triggers a rebuild
2. **Use drafts**: Create files in `_drafts/` for work-in-progress content
3. **Test locally**: Always test changes locally before pushing
4. **Check frontmatter**: Invalid frontmatter will cause build failures
5. **Use data files**: For content that repeats, use `_data/` files

## 🎯 Common Tasks Cheat Sheet

```bash
# Add a new example
touch _examples/my-example.md
# Edit it, commit, and push!

# Add a new user guide
touch _user_guides/my-guide.md
# Edit it, commit, and push!

# Update presentations
nano _data/presentations.yml
# Edit, save, commit, and push!

# Update home page cards
nano _data/home_components.yml
# Edit, save, commit, and push!

# Test locally
bundle exec jekyll serve
# Visit http://localhost:4000/docs/

# Build for production
bundle exec jekyll build
# Output in _site/ directory
```

## 🤝 Contributing

When adding content, please:

1. Use clear, descriptive titles
2. Add proper descriptions in frontmatter
3. Tag content appropriately
4. Test locally before pushing
5. Keep formatting consistent

Happy content creating! 🎉
