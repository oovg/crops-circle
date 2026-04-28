<h1 align="center" style="margin-top: 1em; margin-bottom: 2em;">
  <p>👋 Contributing to CROPS Circle</p>
</h1>

### Thank you for your interest in contributing!

CROPS Circle is a peer-curated index of autonomous technologies — tools that are **Censorship Resistant, Open Source, Private,** and **Secure**. The site is maintained by contributors who add, remove, and refine entries through GitHub. Contributions of any kind are welcome.

Before you start, please take a moment to read our [README.md](README.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

## What qualifies as a CROPS tool

A tool belongs in the index if it meaningfully meets the CROPS criteria:

- **Censorship Resistant** — cannot be removed or blocked by a platform or government
- **Open Source** — source code is publicly available to read, audit, and modify
- **Private** — does not collect or share personal data
- **Secure** — designed to resist unauthorized access and attack

Hardware, operating systems, protocols, applications, and services are all in scope. Centralized SaaS, proprietary stacks, and ad-funded "free" tools are not.

## How to contribute

### 1. Submit an issue

Before opening a PR — especially for additions, removals, or anything that could be contested — open an issue first. This lets the community discuss whether a tool qualifies, where it belongs, and how to describe it.

For tool **suggestions**, include:

- Tool name and URL
- Which CROPS criteria it meets, with brief evidence (license, audit reports, architecture)
- Which section(s) it belongs in
- Why it's worth indexing — especially against anything similar already listed

For tool **removals**, include:

- The tool name
- The reason: project abandoned, license changed, breach of CROPS criteria, replaced by something better, etc.

### 2. Fork the repository

If you're not sure how, here's how to [fork the repo](https://help.github.com/en/articles/fork-a-repo).

### 3. Set up locally

There is no build step, no JavaScript, and no dependencies. To preview your changes:

```sh
git clone git@github.com:[your_github_handle]/cropscircle.git && cd cropscircle
open index.html
```

Or just double-click `index.html` in your file manager. The site is a single static HTML file — what you see in your browser is what visitors will see.

### 4. Make your changes

Everything lives in `index.html`. Each tool may appear in **two places**:

1. **Quiz panel** — curated short-list (~4 tools) shown in the modal under each "What are your technology needs?" answer. Markup begins with `<div class="quiz-answer ans-...">`.
2. **Complete Index** — full per-category list further down the page. Markup begins with `<section id="...">`.

Most tools appear in both. The quiz panel is a top recommendation; the Complete Index is the canonical home.

#### Entry format

Every tool entry is a three-line `<dt>/<dd>/<dd>` triple inside a `<dl>`:

```html
<dt>TOOL NAME</dt>
<dd class="desc">Short technical description; what makes it distinct or sovereign. Optional one-line tagline.</dd>
<dd class="url"><a href="https://example.com">https://example.com</a></dd>
```

Style:

- `<dt>` is uppercase.
- `desc` is roughly 15–30 words. Lead with what the tool is, follow with what makes it CROPS-aligned. The existing entries use a semicolon-separated technical clause + a brief tagline — match that voice.
- `url` repeats the URL as visible text inside the link.

#### Complete Index sections

| Category | Section id |
| --- | --- |
| Hardware & Infrastructure | `hardware` |
| Operating Systems & Firmware | `os` |
| Communication | `communication` |
| Networking & Anonymity | `networking` |
| Data & Storage | `data` |
| Identity & Authentication | `identity` |
| Money & Value Exchange | `money` |
| Search & Browsing | `search` |
| Development & Collaboration | `development` |
| AI & Computation | `ai` |
| Governance & Coordination | `governance` |

#### Quiz panels

| User need | Panel class |
| --- | --- |
| Communicate privately | `ans-communicate` |
| Stay anonymous online | `ans-anonymous` |
| Secure my device | `ans-device` |
| Own my data | `ans-data` |
| Transact without surveillance | `ans-money` |
| Browse without being tracked | `ans-browse` |
| Run my own infrastructure | `ans-infra` |
| Build and collaborate freely | `ans-build` |
| Run AI without the cloud | `ans-ai` |
| Coordinate with my community | `ans-govern` |

Quiz panels currently hold 4 tools each. Five is fine; if you're adding a strong contender, consider whether it should bump an existing entry instead.

*(Note: "Identity & Authentication" has a Complete Index section but no quiz panel.)*

### 5. Submit your PR

- After your changes are committed to your fork, submit a pull request.
- Reference the issue your PR resolves in the description, e.g. `Adds Tool X [Fixes #42]`.
- One tool per PR is preferred unless the change is a coherent batch (e.g., reorganizing a category).
- Confirm your changes look correct by opening `index.html` in a browser before submitting.

### 6. Wait for review

- Maintainers and other contributors review every PR.
- Acceptable PRs will be approved and merged.

### 7. Release

Once merged, changes go live on the next deploy of the static site.

## House rules

- **No JavaScript, no cookies, no trackers.** All interactivity is CSS-only.
- **No CDN dependencies** — no remote fonts, scripts, or images. Assets are local.
- **Keep `index.html` scannable in a plain text editor** — no minification, preserve indentation.

## Questions?

Email us at [cropscircle@protonmail.com](mailto:cropscircle@protonmail.com).
