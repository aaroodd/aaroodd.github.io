# aaroodd.github.io

Personal website of Aaroodd Ujjayini Ramachandran — physics PhD student at [Washington University in St. Louis](https://wustl.edu).

**Live site:** [aaroodd.github.io](https://aaroodd.github.io)

## About

Built with [Jekyll](https://jekyllrb.com/) using the [al-folio](https://github.com/alshedivat/al-folio) theme (v0.16.3). Features include:

- Inline CV rendered from YAML
- BibTeX-driven publications with INSPIRE-HEP badges
- Categorized project cards (research & technical)
- Live market data via TradingView widgets
- Blog with MathJax support
- Dark/light mode, search, responsive design

## Local development

Requires Ruby and Bundler:

```bash
bundle install
bundle exec jekyll serve
```

Then open [localhost:4000](http://localhost:4000).

## Deployment

Pushes to `main` trigger a GitHub Actions workflow that builds the site and deploys to the `gh-pages` branch. GitHub Pages serves from `gh-pages`.

## Credits

- [al-folio](https://github.com/alshedivat/al-folio) theme by Maruan Al-Shedivat
- Originally based on [Particle](https://github.com/nrandecker/particle) by Nathan Randecker
- Built with [Claude](https://claude.ai)
