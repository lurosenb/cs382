# course site template

a quarto-based course website. fork or copy this folder for each new course offering.

---

## prerequisites

install [quarto](https://quarto.org/docs/get-started/). no other dependencies.

```bash
# render to docs/
quarto render

# live preview with hot reload
quarto preview
```

---

## what to customize

### 1. brand color — `styles.css`

change the three css variables at the top of the file. everything (navbar, table headers, section dividers, proof block borders) updates automatically.

```css
:root {
  --brand-color: #362061;       /* navbar and table header background */
  --brand-color-light: #5a3d8a; /* section-header row background */
  --brand-color-tint: #ede8f5;  /* alternating table row background */
  --brand-accent: #FECC06;      /* proof block border */
}
```

### 2. site metadata — `_quarto.yml`

fill in `[SEMESTER]`, `[DISCORD_URL]`, and `[GRADESCOPE_URL]`. these control the navbar title and links.

### 3. landing page — `index.qmd`

the yaml comment block at the top lists every `[PLACEHOLDER]` in the file. fill in the two-column info block and duplicate/fill the week rows in the schedule table. each row type (lecture, midterm, break) has a labeled example.

### 4. syllabus — `syllabus.qmd`

same pattern — yaml comment block lists all placeholders. replace the bracketed descriptions with course-specific language.

### 5. lecture notes — `notes/`

`00_template_lecture.qmd` is the note template. for each lecture:

1. copy it to `notes/NN_topic_name.qmd`
2. fill in `[LECTURE_TITLE]` and the section content
3. drop any figures into `notes/images/`
4. link the rendered html from the schedule table in `index.qmd`

### 6. slides and problem sets

- drop weekly slide pdfs into `slides/` as `Week01.pdf`, `Week02.pdf`, etc.
- drop problem set notebooks into `psets/starter_code/` — they are copied as static assets on render.

### 7. analytics — `header.html`

the google analytics block is commented out. uncomment and replace `[GA_MEASUREMENT_ID]` to enable it.

---

## hosting on github pages

### setup

1. create a new github repo (e.g. `lucasrosenblatt/cs382_rml`).
2. add a `.nojekyll` file to `docs/` so github does not reprocess the output:
   ```bash
   touch docs/.nojekyll
   ```
3. set `site-url` in `_quarto.yml`:
   ```yaml
   website:
     site-url: https://lucasrosenblatt.github.io/cs382_rml
   ```
4. push to github. in the repo settings → pages, set the source to **branch: main, folder: /docs**.
5. the site is live at `https://lucasrosenblatt.github.io/cs382_rml`.

### custom subdomain (e.g. `cs382.lucasrosenblatt.com`)

1. add a `CNAME` file to the repo root containing the subdomain:
   ```
   cs382.lucasrosenblatt.com
   ```
2. add it as a resource in `_quarto.yml` so it survives renders:
   ```yaml
   project:
     resources:
       - CNAME
   ```
3. update `site-url` to the subdomain.
4. in the domain registrar's dns settings, add a CNAME record pointing `cs382` → `lucasrosenblatt.github.io`.
5. in the repo settings → pages, enter the custom domain and enable "enforce https".

### custom path (e.g. `lucasrosenblatt.com/courses/cs382_rml`)

github pages does not support hosting at a subdirectory of a domain it does not fully control. the options are:
- use `lucasrosenblatt.github.io/cs382_rml` directly, or
- use a subdomain as above, or
- configure a reverse proxy on whatever server hosts `lucasrosenblatt.com` to forward `/courses/cs382_rml` → `lucasrosenblatt.github.io/cs382_rml`.
