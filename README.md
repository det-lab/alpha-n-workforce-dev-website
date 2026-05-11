# alpha, n Workforce Development Program Website

Static website for the alpha, n Workforce Development Program, built with Jekyll and hosted on GitHub Pages.

## Live site

> **URL:** `https://det-lab.github.io/alpha-n-workforce-dev-website/`

---

## How to update content

All site content lives in two places: the `_data/` folder (for structured content like people and resources) and `index.md` (for the home page text). You do not need to touch any HTML or CSS to update content.

### Add or edit students

Open `_data/students.yml`. Each cohort year has a list of students:

```yaml
cohorts:
  - year: 2025
    students:
      - name: "Jane Smith"
        bio: "Jane is a second-year PhD student in Computer Science."
        program: "Computer Science"
        photo: "/assets/images/jane-smith.jpg"   # leave as "" if no photo
```

- To add a new student, copy one block and fill in the fields.
- To add a new cohort year, add a new `- year:` block above the existing ones (most recent year first).
- Photos: save the image file to `assets/images/` and set the `photo:` field to `/assets/images/filename.jpg`.

### Add or edit staff

Open `_data/staff.yml`. Each staff member is one block:

```yaml
- name: "Dr. Alex Johnson"
  title: "Program Director"
  bio: "Alex directs the program and coordinates with partner institutions."
  email: "alex.johnson@example.edu"
  photo: "/assets/images/alex-johnson.jpg"   # leave as "" if no photo
```

### Add or edit resources

Open `_data/resources.yml`. Resources are organized by category:

```yaml
- category: "Getting Started"
  items:
    - title: "Program Handbook"
      description: "Covers expectations, policies, and procedures."
      url: "https://example.edu/handbook"
```

- To add a new resource, add a `- title:` block under the appropriate category.
- To add a new category, add a new `- category:` block.
- Set `url: "#"` for a resource that doesn't have a link yet — it will display as "Coming soon."

### Edit the home page text

Open `index.md` and edit the text in the About section near the bottom of the file.

---

## How to deploy / update the live site

After editing any file, commit and push to the `main` branch:

```bash
git add .
git commit -m "Update student list for 2025 cohort"
git push
```

GitHub Pages rebuilds the site automatically within about a minute. No other steps are needed.

---

## First-time setup (if not yet deployed)

1. Create a GitHub repository.
2. In `_config.yml`, update:
   ```yaml
   baseurl: "/your-repo-name"
   url: "https://det-lab.github.io"
   ```
3. Connect the remote and push:
   ```bash
   git remote add origin https://github.com/det-lab/REPO-NAME.git
   git push -u origin main
   ```
4. In the GitHub repo go to **Settings → Pages → Source** and select `main` branch, `/ (root)` folder.

## Local preview (optional)

Requires Ruby and Bundler. From the project root:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000/alpha-n-workforce-dev-website/` in a browser.
