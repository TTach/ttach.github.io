# Copilot Instructions for ttach.github.io

## Project Overview
This is a GitHub Pages repository (`ttach.github.io`) that serves as a personal website/portfolio hosted at https://ttach.github.io.

## Technology Stack
- **Hosting**: GitHub Pages (static site hosting)
- **Domain**: `ttach.github.io` (GitHub's default user pages domain)
- **Current State**: Minimal setup with only README.md

## Development Workflow

### Local Development
```bash
# GitHub Pages supports static HTML/CSS/JS or Jekyll
# For Jekyll (if used):
bundle exec jekyll serve --livereload

# For static sites, use any local server:
python3 -m http.server 8000
# or
npx serve
```

### Deployment
- Push to `main` branch - GitHub Pages automatically deploys
- Site typically available within 1-2 minutes of push
- Check deployment status at: https://github.com/TTach/ttach.github.io/actions

## Project-Specific Conventions

### File Organization
- Root-level `index.html` (or `index.md` for Jekyll) serves as the homepage
- Assets typically organized in `assets/`, `css/`, `js/`, `images/` directories
- Jekyll sites use `_posts/`, `_layouts/`, `_includes/` directories with underscore prefix

### GitHub Pages Constraints
- **Static content only** - no server-side processing
- **File size limit**: Individual files should be < 100 MB
- **Site size limit**: Published site should be < 1 GB
- **Build time limit**: 10 minutes for Jekyll builds
- Supported Jekyll themes: https://pages.github.com/themes/

## Common Tasks

### Adding a New Page
Create an HTML or Markdown file in the root or subdirectory:
```bash
touch about.html
# Accessible at: https://ttach.github.io/about.html
```

### Setting Up Jekyll (if desired)
```bash
# Create Gemfile
echo 'source "https://rubygems.org"' > Gemfile
echo 'gem "github-pages", group: :jekyll_plugins' >> Gemfile
bundle install

# Create _config.yml with site configuration
# Create _layouts/default.html for page template
```

### Custom Domain Setup
- Add `CNAME` file in root with custom domain name
- Configure DNS records at domain registrar
- Enable HTTPS in repository settings

## Best Practices

- **Test locally first**: Always preview changes before pushing
- **Optimize assets**: Compress images and minify CSS/JS for faster load times
- **Mobile-first**: Design responsively - GitHub Pages are often viewed on mobile
- **SEO basics**: Include proper meta tags, Open Graph tags for social sharing
- **Avoid sensitive data**: This is a public repository - never commit API keys or credentials

## Useful References
- GitHub Pages docs: https://docs.github.com/pages
- Jekyll docs (if using): https://jekyllrb.com/docs/
- GitHub Pages dependency versions: https://pages.github.com/versions/
