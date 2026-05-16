# Jiangrui Kang Personal Homepage

Source for [jiangruikang.github.io](https://jiangruikang.github.io/), a Jekyll-based academic personal homepage.

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000>.

The repository is configured for GitHub Pages through the `github-pages` gem.

## Main Files

- Site configuration and profile links: `_config.yml`
- Homepage content: `_pages/about.md`
- Top navigation: `_data/navigation.yml`
- Profile sidebar template: `_includes/author-profile.html`
- Google Scholar citation script: `_includes/fetch_google_scholar_stats.html`

## Notes

- Keep publication entries factual and avoid placeholder template content.
- Set `author.googlescholar` in `_config.yml` only after replacing the placeholder with a real Google Scholar profile URL.
- Generated output in `_site/` is ignored by Git.

## Acknowledgements

This site is based on [AcadHomepage](https://github.com/RayeRen/acad-homepage.github.io), which incorporates Font Awesome and is influenced by `mmistakes/minimal-mistakes` and `academicpages/academicpages.github.io`.
