# Wildfire ML Lab Website

A Jekyll-based GitHub Pages website with four pages:
**Home · Publications · People · Blog Posts**

---

## Editing Content

All content lives in plain text (Markdown `.md`) files. No web development knowledge is needed to update them.

### Home Page
Edit `index.md` to change the text on the home page.

### Publications
Each publication is a file in `_publications/`. Copy `paper_template.md`, rename it with the date and paper slug (e.g. `2024-03-01-wildfire-detection.md`), and fill in the fields at the top of the file.

**Fields explained:**
- `title` — paper title
- `category` — `manuscripts` for journal articles, `conferences` for conference papers
- `date` — publication date in `YYYY-MM-DD` format (controls sort order)
- `venue` — journal or conference name
- `excerpt` — one-line description shown in the list
- `paperurl` / `bibtexurl` / `slidesurl` — optional download links (delete any you don't have)
- `citation` — full citation text shown at the bottom of the paper page

Write a longer description below the `---` line. It appears when someone clicks through to the paper.

### People
Each person is a file in `_people/`. Copy an existing file, rename it (e.g. `jane_smith.md`), and fill in the title and bio.

To add a photo: upload an image to the `images/` folder, then reference it in the `excerpt` line like:
```
excerpt: "PhD Student<br/><img src='/images/jane_smith.jpg'>"
```

### Blog Posts
Each post is a file in `_posts/`. The filename **must** follow the format `YYYY-MM-DD-post-slug.md` (e.g. `2024-06-01-field-season-recap.md`). Fill in the `title` and `date` fields, then write your post below the `---` line using Markdown.

---

## Site Settings

Open `_config.yml` to change:
- **Site title, description, URL** — under `# Basic Site Info`
- **Sidebar author info** (name, bio, photo, GitHub, email, etc.) — under `# Sidebar Author Profile`
- **Navigation links** — edit `_data/navigation.yml`
- **Publication categories** — under `# Publication Categories`
- **Analytics** — under `# Analytics`

---

## Adding Images

Upload image files into the `images/` folder. Reference them in Markdown as:
```
![Alt text](/images/your-image.jpg)
```
Or in a people/publication excerpt as `<img src='/images/your-image.jpg'>`.

---

## Running Locally (optional)

Requires Ruby and Bundler. From the project root:
```bash
bundle install
bundle exec jekyll serve
```
Then open `http://localhost:4000` in your browser.

---

## File Structure

```
_config.yml          ← site settings (start here)
index.md             ← home page content
_data/
  navigation.yml     ← top nav links
_pages/
  publications.html  ← Publications page (no editing needed)
  people.html        ← People page (no editing needed)
  year-archive.html  ← Blog Posts page (no editing needed)
_publications/       ← one .md file per paper
_people/             ← one .md file per person
_posts/              ← one .md file per blog post
images/              ← photos and favicons
assets/              ← CSS, JS, fonts (no editing needed)
_layouts/            ← page templates (no editing needed)
_includes/           ← reusable HTML snippets (no editing needed)
_sass/               ← stylesheets (no editing needed)
```
