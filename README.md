# yubohuangai.github.io

Personal academic homepage for **Yubo Huang** — https://yubohuangai.github.io/

Built with Jekyll. The design is adapted from [Jon Barron's website](https://jonbarron.info)
via [Leonid Keselman's Jekyll fork](https://github.com/leonidk/leonidk.github.io)
(itself built on [Jekyll Now](https://github.com/barryclark/jekyll-now)). Only the
design shell is reused; all content is Yubo Huang's own. See `LICENSE` for the
template's MIT licence.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Editing

- Profile fields, links → `_config.yml`
- Home page (about / research / publications) → `index.md`
- Publications data → `_data/publications.yml`
- Motion Capture page → `motion-capture.md`
- Layout markup → `_layouts/default.html`
- Styles (Barron-style base + responsive breakpoints) → `style.scss`
