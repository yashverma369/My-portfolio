# Maintenance guide

How to keep the portfolio up to date. All content that changes often lives in one data block in `index.html`, so no build or tooling is needed.

## Turn on GitHub Pages (one time)

1. Open the repository on GitHub and go to **Settings**, then **Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select the `main` branch and the `/ (root)` folder, then save.
4. Wait a minute or two. The site opens at `https://yashverma369.github.io/My-portfolio/`.

## The data block

Near the top of `index.html`, below the line `<div id="root"></div>`, there is a block like this:

```html
<script id="site-data" type="application/json">
{
  "projects": [],
  "resume": {
    "name": "Yash_Kumar_Resume.pdf",
    "file": "Yash_Kumar_Resume.pdf",
    "size": 56562,
    "updated": "2026-10-09"
  }
}
</script>
```

It must stay valid JSON: double quotes around every key and text value, commas between items, and no comma after the last item.

## Add a new project

Add an object to the `projects` list and keep the `resume` part unchanged:

```json
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
```

| Field | Notes |
| --- | --- |
| `id` | Required. Use a different value for every project. |
| `title`, `desc` | Required. |
| `tag` | Short label, for example "Personal project". |
| `status` | `Live`, `In progress` or `Completed`. |
| `tech` | Up to 8 technologies. |
| `demo`, `repo` | Optional. Must start with `https://`. |

Several projects go in the same list, separated by commas. Commit the change and the site updates automatically.

## Update the resume

1. In the repository, choose **Add file**, then **Upload files**.
2. Upload the new PDF with the same name, `Yash_Kumar_Resume.pdf`, and commit. It replaces the old file.
3. Optional: update `size` (in bytes) and `updated` (as `YYYY-MM-DD`) in the data block so the line under the download button stays correct.

The resume contains a phone number and an email address, and anyone who has the site link can download it.

## Admin panel

An Admin button exists only on the copy of this portfolio hosted on claude.ai. It does not appear on GitHub Pages, and changes made there do not change this repository.
