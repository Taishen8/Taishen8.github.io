# Gan Haipeng — Academic Portfolio (Jekyll)

This repository is a Jekyll site using the Minimal Mistakes theme. It is structured as a scrollable research landing page with linked research posts and media pages.

## Quick Start (Local Preview)

Ruby is installed at `C:\Ruby34-x64` on this machine.

```bash
"/c/Ruby34-x64/bin/ruby.exe" "C:\Users\poten\Desktop\assets\Taishen8.github.io\bin\jekyll" serve
```

Open http://localhost:4000 in your browser.

If you move the repo or Ruby location changes, re-run Bundler:

```bash
"/c/Ruby34-x64/bin/bundle.bat" install
```

## Where to Edit

### Homepage
- `index.markdown`
  - Hero section (name, tagline, buttons)
  - Research focus cards
  - Media gallery
  - Ongoing projects
  - Publication block
  - Research notes list

### Site Metadata
- `_config.yml`
  - name, bio, email, scholar link, CV link, GitHub, description

### Styling
- `_sass/custom/custom.scss`
  - Bold visual styles (cards, CTA, typography, accents)
- `_includes/head/custom.html`
  - Fonts and global font overrides

### Posts (Research Notes)
All deep-dive posts are in `_posts/`.

Core project posts:
- `2026-01-22-peptide-catalysts-discovery.markdown`
- `2026-01-22-peptide-assembly-llm-mining.markdown`
- `2026-01-22-rl-material-generation.markdown`

Media posts:
- `2026-01-22-media-binding-dynamics.markdown`
- `2026-01-22-media-catalytic-motif-screening.markdown`
- `2026-01-22-media-assembly-mechanism.markdown`
- `2026-01-22-media-rl-trajectories.markdown`
- `2026-01-22-media-llm-extraction.markdown`
- `2026-01-22-media-molecular-movie.markdown`

## Media Files

Place MP4 files here:

```
assets/media/
```

Expected filenames (replace or rename in posts if you choose different names):
- `peptide-binding-dynamics.mp4`
- `catalytic-motif-screening.mp4`
- `peptide-assembly-mechanism.mp4`
- `rl-trajectories.mp4`
- `llm-extraction-pipeline.mp4`
- `molecular-movie-highlight.mp4`

Poster images are referenced in `assets/images/` with matching placeholders. Replace them with your real figures.

## Adding a New Project or Media Post

1. Add a new Markdown file under `_posts/` with a date prefix.
2. Use the research-style structure:
   - Abstract
   - Motivation
   - Methods
   - Results (figures/movies)
   - Current Status
   - Next Steps
3. Add a new card in `index.markdown` under the media or project sections.

## Deploy

Push to GitHub and enable GitHub Pages for the repo. The site will publish automatically.
