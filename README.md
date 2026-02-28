# retiredthinkercomments

GitHub repository used as the backend for [utterances](https://utteranc.es/) comments on [retiredthinker.com](https://retiredthinker.com).

## What is utterances?

[utterances](https://utteranc.es/) is a lightweight, open-source comments widget built on GitHub Issues. When a visitor leaves a comment on the site, utterances creates a GitHub Issue in this repository to store it.

## Setup

### 1. Install the utterances GitHub App

The repository owner must install the utterances app and grant it access to this repository:

👉 [Install utterances app](https://github.com/apps/utterances)

Select **Only select repositories** and choose `DrProton92/retiredthinkercomments`.

### 2. Embed the widget on retiredthinker.com

Add the following script tag to each page where you want comments to appear (typically at the bottom of each post/page template):

```html
<script src="https://utteranc.es/client.js"
        repo="DrProton92/retiredthinkercomments"
        issue-term="pathname"
        label="comments"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
```

The ready-to-use snippet is also available in [`utterances.html`](./utterances.html).

### Configuration options

| Attribute | Value | Description |
|-----------|-------|-------------|
| `repo` | `DrProton92/retiredthinkercomments` | This repository |
| `issue-term` | `pathname` | Maps each page URL path to a unique GitHub Issue |
| `label` | `comments` | Label added to every comment issue |
| `theme` | `github-light` | Widget theme (see [utteranc.es](https://utteranc.es) for alternatives) |

### Available themes

- `github-light` *(default)*
- `github-dark`
- `preferred-color-scheme` *(follows the visitor's OS preference)*
- `github-dark-orange`
- `icy-dark`
- `dark-blue`
- `photon-dark`
- `boxy-light`
- `gruvbox-dark`

## Moderating comments

All comments are stored as GitHub Issues in this repository. You can moderate them (edit, close, lock, or delete) directly from the [Issues tab](../../issues).

