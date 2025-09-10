# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is a Jekyll-based academic personal homepage built on the AcadHomepage theme. It's designed for GitHub Pages hosting and includes automated Google Scholar citation crawling.

## Development Commands

### Local Development
```bash
# Start Jekyll development server with live reload
bash run_server.sh
# OR
bundle exec jekyll liveserve

# Access site at: http://127.0.0.1:4000
```

### Dependencies
```bash
# Install Ruby dependencies
bundle install

# Install Python dependencies for Google Scholar crawler
cd google_scholar_crawler
pip3 install -r requirements.txt
```

## Architecture

### Key Directories
- `_pages/`: Main content pages (about.md contains homepage content)
- `_includes/`: Jekyll template partials (author-profile.html, seo.html, etc.)
- `_layouts/`: Page layouts (default.html)
- `_sass/`: SCSS stylesheets
- `_data/`: Site data files (navigation.yml)
- `google_scholar_crawler/`: Python script for automated citation data collection
- `images/`: Static images including favicon files
- `assets/`: Static assets

### Configuration Files
- `_config.yml`: Main Jekyll configuration with site metadata, author info, and plugin settings
- `Gemfile`: Ruby gem dependencies (uses github-pages gem for GitHub Pages compatibility)

### Google Scholar Integration
- Automated GitHub Action (`.github/workflows/google_scholar_crawler.yaml`) runs daily at 08:00 UTC
- Requires `GOOGLE_SCHOLAR_ID` secret to be configured in repository settings
- Generates citation data in `google-scholar-stats` branch as `gs_data.json`
- Citations displayed using `<span class='show_paper_citations' data='PAPER_ID'></span>` tags

### Content Structure
- Homepage content is in `_pages/about.md`
- Uses Jekyll Liquid templating for dynamic content
- Supports HTML + Markdown syntax
- Author profile sidebar configured in `_config.yml` under `author:` section

### Key Features
- Responsive design with automatic screen size adaptation
- SEO optimization with configurable meta tags
- Google Analytics integration (optional)
- Automatic favicon generation support
- Citation display with Google Scholar paper IDs
- GitHub Pages compatible deployment

### Styling
- SCSS-based styling in `_sass/` directory
- Compressed CSS output for production
- Custom variables and responsive design patterns
- Font Awesome icon integration