# OSS Shortlist

Compare a handful of GitHub projects side by side before picking a dependency, framework, or tool. OSS Shortlist shows repository facts and maintenance signals next to each other instead of turning them into an unexplained score.

[![GitHub stars](https://img.shields.io/github/stars/X234324/oss-shortlist?style=social)](https://github.com/X234324/oss-shortlist)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](./LICENSE)

**[Try OSS Shortlist online](https://x234324.github.io/oss-shortlist/)** · No install, account, token, or backend.

The first time you publish, enable **Settings → Pages → Deploy from a branch → `main` / `/(root)`**. GitHub Pages then serves the app directly from this repository.

## Why another GitHub tool?

GitHub is great for inspecting one repository. OSS Shortlist is for the moment you have several candidates and want a quick, shareable comparison: recent code push, latest release, license, archived status, stars, forks, and open issues — all in one view. It deliberately does not claim that stars or activity prove quality or security.

## Use it

Open [`index.html`](./index.html) in a browser, add up to four repositories, and compare. Paste either `owner/repo` or a GitHub repository URL. Sample comparisons are included.

You can copy a Markdown report anywhere. After publishing the page, use **Copy share link** to share the exact comparison; the selected repository names live in the URL fragment.

## Run it yourself

Open [`index.html`](./index.html) in a browser, or serve this folder locally:

```powershell
python -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000). No build step is required.

## What the signals mean

- **Archived** — the repository owner marked it read-only.
- **Code push older than 180 days** and **latest release older than 365 days** — configurable in the source constants, shown as separate prompts rather than a combined verdict.
- **No declared license** — reuse terms may be unclear; check the repository before using the code.
- A missing GitHub Release is reported as “none published,” not a finding against projects that distribute another way.

The app reads the public GitHub REST API directly from your browser. It stores no data, requests no credentials, and includes no analytics or third-party JavaScript. GitHub's unauthenticated API limit is 60 requests per hour; each checked repository uses up to two requests.

For deeper supply-chain security checks, see [OpenSSF Scorecard](https://github.com/ossf/scorecard). OSS Shortlist is a comparison aid, not a security audit or quality ranking.

## Contributing

Bug reports, accessibility improvements and focused feature requests are welcome. Please keep comparisons evidence-based and avoid adding opaque quality scores. If OSS Shortlist helped with a decision, a star helps other people discover it.

## License

MIT. See [`LICENSE`](./LICENSE).
