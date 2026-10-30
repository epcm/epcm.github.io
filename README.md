# epcm.github.io

Personal academic website of **Kaiyuan Zhang**, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll starter (v1.x).

Live site: <https://epcm.github.io>

## What to edit

| Content                        | File(s)                                           |
| ------------------------------ | ------------------------------------------------- |
| Site title, URL, feature flags | `_config.yml`                                     |
| Bio / home page                | `_pages/about.md`                                 |
| Profile photo                  | `assets/img/prof_pic.jpg`                         |
| Publications                   | `_bibliography/papers.bib` (+ `_data/venues.yml`) |
| CV (web version)               | `_data/cv.yml`                                    |
| CV (PDF download)              | `assets/pdf/Kaiyuan_Zhang_CV.pdf`                 |
| News items                     | `_news/*.md`                                      |
| Social links / email           | `_data/socials.yml`                               |

### Publications

Each BibTeX entry supports extra fields: `abbr` (venue badge, colors in `_data/venues.yml`), `selected = {true}` (shows on the home page), `award` / `award_name`, `pdf`, `html`, `code`, `slides`, `poster`, `arxiv`, `preview` (thumbnail in `assets/img/publication_preview/`), and `bibtex_show`.

## Deploy (GitHub Pages)

1. Create a **public** repository named `epcm.github.io` and push this folder to the `main` branch.
2. In the repository go to **Settings → Actions → General → Workflow permissions** and select **Read and write permissions**.
3. The `Deploy site` workflow (`.github/workflows/deploy.yml`) builds the site and pushes the result to a `gh-pages` branch.
4. In **Settings → Pages**, set _Source_ to **Deploy from a branch**, branch **`gh-pages`**, folder **`/ (root)`**.
5. After a minute or two the site is live at <https://epcm.github.io>.

## Run locally

With Docker:

```bash
docker compose up
# open http://localhost:8080
```

Or with Ruby ≥ 3.3:

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

## License

Template © al-folio contributors, MIT License (see `LICENSE`). Site content © Kaiyuan Zhang.
