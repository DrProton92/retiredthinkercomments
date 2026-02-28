# retiredthinkercomments

Comments repository for [retiredthinker.com](https://retiredthinker.com), powered by [utterances](https://utteranc.es/).

## About

This repository stores comments for retiredthinker.com as GitHub Issues using the [utterances](https://github.com/marketplace/utterances) GitHub App.

## Setup

### 1. Install the utterances GitHub App

Install the [utterances app](https://github.com/apps/utterances) and grant it access to this repository (`DrProton92/retiredthinkercomments`).

### 2. Embed the widget on your website

Add the following `<script>` tag to each page on retiredthinker.com where you want comments to appear (e.g., inside your post template, just before the closing `</body>` tag):

```html
<script src="https://utteranc.es/client.js"
        repo="DrProton92/retiredthinkercomments"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
```

#### Configuration options

| Attribute | Description |
|-----------|-------------|
| `repo` | The GitHub repository where issues (comments) are stored. |
| `issue-term` | How a page maps to a GitHub Issue. `pathname` is recommended; other options: `url`, `title`, `og:title`. |
| `theme` | Widget theme. Options: `github-light`, `github-dark`, `preferred-color-scheme`, `github-dark-orange`, `icy-dark`, `dark-blue`, `photon-dark`, `boxy-light`. |
| `crossorigin` | Must be `anonymous`. |

## How it works

- When a visitor opens a page, the utterances widget searches for a GitHub Issue in this repository matching the page URL/pathname.
- If no issue exists yet, the utterances bot creates one automatically when the first comment is submitted.
- Visitors authenticate with GitHub to post comments.
- All comments are stored as GitHub Issue comments and are visible both on retiredthinker.com and in this repository's [Issues](../../issues) tab.
