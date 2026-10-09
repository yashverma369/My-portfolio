# Yash Kumar | Portfolio

Personal portfolio of Yash Kumar, B.Tech student and aspiring Software / Web Developer from Noida.

Live site: https://yashverma369.github.io/My-portfolio/ (opens once GitHub Pages is turned on, see below)

Built with React, Tailwind CSS and GSAP. There is no build step.

## Files

- `index.html`: the whole site.
- `Yash_Kumar_Resume.pdf`: the file the Resume section downloads.

## Run locally

Open `index.html` in a browser. An internet connection is needed because React, Tailwind and GSAP load from a CDN.

## Deploy on GitHub Pages

1. Open the repository on GitHub and go to Settings, then Pages.
2. Under Build and deployment, choose Deploy from a branch.
3. Select the `main` branch and the `/ (root)` folder, then save.
4. Wait a minute or two. The site opens at `https://yashverma369.github.io/My-portfolio/`.

## Add a new project

Projects live in one block near the top of `index.html`, under the line `<div id="root"></div>`:

```html
<script id="site-data" type="application/json">{"projects":[],"resume":{ ... }}</script>
```

Add each new project inside the `projects` list and leave the `resume` part as it is. Example:

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
  ],
  "resume": {
    "name": "Yash_Kumar_Resume.pdf",
    "file": "Yash_Kumar_Resume.pdf",
    "size": 56562,
    "updated": "2026-10-09"
  }
}
</script>
```

- `status` can be `Live`, `In progress` or `Completed`.
- `demo` and `repo` are optional and must start with `https://`.
- Give every project a different `id` and separate projects with commas.

Commit the change and GitHub Pages updates the site in a minute or two.

## Update the resume

1. In the repository, choose Add file, then Upload files.
2. Upload the new PDF with the same name, `Yash_Kumar_Resume.pdf`, and commit. It replaces the old file.
3. Optional: in the `site-data` block of `index.html`, update `size` (in bytes) and `updated` (as YYYY-MM-DD) so the line under the download button stays correct.

The resume PDF contains a phone number and email address, and anyone with the site link can download it.

## Admin panel

The Admin button is only available on the copy of this portfolio hosted on claude.ai. It does not appear on GitHub Pages. Changes made there do not change this repository, so update projects and the resume here as described above.
