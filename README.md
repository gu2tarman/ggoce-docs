# GGO CE Docs

GGO CE, GGO Custom Launcher, and GGO scripts user documentation site.

This folder is designed to become its own GitHub repository later. It uses
Material for MkDocs so guides can be written as plain Markdown and deployed to
GitHub Pages.

## Local Preview

```powershell
python -m pip install -r requirements.txt
python -m mkdocs serve
```

Then open:

```text
http://127.0.0.1:8000/
```

## Deploy

Push this folder as the root of a GitHub repository and enable GitHub Pages with
GitHub Actions. The workflow in `.github/workflows/pages.yml` builds and
publishes the site automatically.

## Web Editing

This repository is ready for Pages CMS.

1. Push this folder as the root of a GitHub repository.
2. Open `https://app.pagescms.org`.
3. Sign in with GitHub.
4. Install the Pages CMS GitHub App for the docs repository.
5. Open the repository and edit pages through the web UI.

Images uploaded through the CMS are stored in:

```text
docs/assets/images/
```

The current media URL output assumes the docs site is served at:

```text
https://gu2tarman.github.io/ggoce-docs/
```

If a custom domain such as `https://docs.example.com/` is used later, update
`.pages.yml` media output to `/assets/images`.

## Suggested Launcher Links

After the site URL is decided, add links like these to the launcher sidebar:

```json
{ "label": "가이드", "url": "https://<owner>.github.io/<repo>/" }
{ "label": "설정 가이드", "url": "https://docs.google.com/presentation/d/1iA6vzvoBJPdn_FnCCv4HwOVrhrgPSv4OAhWop-rcqAo/present?usp=sharing" }
{ "label": "CE 기능 위키", "url": "https://<owner>.github.io/<repo>/ce/features/" }
{ "label": "버그 제보", "url": "https://github.com/<owner>/<repo>/issues/new?template=bug_report.yml" }
{ "label": "기능 제안", "url": "https://github.com/<owner>/<repo>/issues/new?template=feature_request.yml" }
```
