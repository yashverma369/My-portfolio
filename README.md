# Yash Kumar | Portfolio

Personal portfolio of Yash Kumar, B.Tech student and aspiring Software / Web Developer from Noida.

Built with React, Tailwind CSS and GSAP. It is a single `index.html` file with no build step.

## Run locally

Open `index.html` in a browser. An internet connection is needed because React, Tailwind and GSAP load from a CDN.

## Deploy on GitHub Pages

1. Push `index.html` to the `main` branch of this repository.
2. Go to Settings, then Pages.
3. Under Build and deployment, choose Deploy from a branch, select `main` and `/ (root)`, and save.
4. The site goes live in a minute at `https://yashverma369.github.io/<repository-name>/`. If the repository is named `yashverma369.github.io`, the address is `https://yashverma369.github.io/`.

## Add a new project

Open `index.html` and find this line near the top of the file:

```html
<script id="site-data" type="application/json">{"projects":[]}</script>
```

Put each new project inside the `projects` list. Example:

```html
<script id="site-data" type="application/json">
{
  "projects": [
    {
      "id": "p1",
      "title": "Quiz App",
      "tag": "Personal project",
      "status": "Live",
      "desc": "A quiz app with a timer and score history.",
      "tech": ["React", "Tailwind CSS"],
      "demo": "https://yashverma369.github.io/quiz-app",
      "repo": "https://github.com/yashverma369/quiz-app"
    }
  ]
}
</script>
```

- `status` can be `Live`, `In progress` or `Completed`.
- `demo` and `repo` are optional and must start with `https://`.
- Use a different `id` for every project and separate projects with commas.

Commit the change and GitHub Pages updates the site automatically.

## Update the resume

The Resume section downloads `Yash_Kumar_Resume.pdf` from this repository.

1. In the repository, choose Add file, then Upload files.
2. Upload the new PDF with the **same name**, `Yash_Kumar_Resume.pdf`, and commit. It replaces the old file.
3. Optional: in `index.html`, update `size` (in bytes) and `updated` (date as YYYY-MM-DD) inside the `site-data` block so the line under the button stays correct.

The Admin button is only available on the copy of this page hosted on claude.ai. On GitHub Pages, change the PDF and the `site-data` block as described above.
