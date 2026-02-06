# Academic Research Website

A clean, data-driven academic website built with **Jekyll**. This stack keeps content in simple YAML files for easy updates, while Jekyll generates a fast, static site that works well with GitHub Pages and stays low-maintenance over time.

## Why Jekyll (brief justification)
- **Static + maintainable**: content lives in `_data` files and Markdown pages, keeping layout separate.
- **GitHub Pages ready**: deploys with a simple push.
- **Easy updates**: add news/publications without touching layout files.

## Quick Start (local)
```bash
bundle install
bundle exec jekyll serve
```

## Build for production
```bash
bundle exec jekyll build
```

## Content workflow
### Add a News update
1. Open `_data/news.yml`.
2. Add a new entry at the top:
   ```yaml
   - date: "YYYY-MM-DD"
     title: "Update title"
     description: "One-sentence summary."
     link: "https://optional-link"
   ```
3. Save and commit.

### Add or update a publication
1. Open `_data/publications.yml`.
2. Add or edit an entry:
   ```yaml
   - title: "Paper title"
     authors: "Author list"
     venue: "Journal or conference"
     year: 2024
     type: "Journal Article"
     links:
       pdf: "https://..."
       doi: "https://doi.org/..."
       code: "https://..."
       slides: "https://..."
   ```
3. Save and commit.

### Update your profile
Edit `_data/profile.yml` for your bio, affiliations, interests, contact info, and CV link.

## Deployment
Push to GitHub Pages (or your hosting of choice). With GitHub Pages, use the default Pages build or a GitHub Actions workflow as preferred.

## GitHub + Local Workflow Commands
### Initialize repository and first commit
```bash
git init
git checkout -b main
git add .
git commit -m "Initial academic website build"
```

### Connect to a private GitHub repository
```bash
git remote add origin git@github.com:YOUR-USERNAME/YOUR-PRIVATE-REPO.git
git push -u origin main
```

### Clone locally and open in VS Code
```bash
git clone git@github.com:YOUR-USERNAME/YOUR-PRIVATE-REPO.git
cd YOUR-PRIVATE-REPO
code .
```

### Install dependencies, run locally, and build
```bash
bundle install
bundle exec jekyll serve
bundle exec jekyll build
```

## Update Workflow (short)
- **Add a News post**: edit `_data/news.yml` and commit.
- **Add/update a Publication**: edit `_data/publications.yml` and commit.
- **Deploy updates**: push to `main` (GitHub Pages rebuilds automatically).

## Design Rationale (distinct from reference)
- **Visual identity**: warm cream/forest palette, serif body + geometric sans headings, and rounded card system (distinct from the reference aesthetic).
- **Layout**: hero panel + split research snapshot, timeline-based news, and rounded list cards.
- **Spacing**: custom spacing scale and wider section rhythm create a different flow and hierarchy.

## Project Tree (key directories)
```
.
├── _data
├── _includes
├── _layouts
├── _pages
├── _sass
├── assets
├── files
└── images
```
