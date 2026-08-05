# Tender Violet Studio

Tender Violet, a New Jersey based design & website development studio, that specializes in weddings. Plain HTML/CSS/JS — no build step, deploys straight to GitHub Pages.

## Structure

```
index.html        Home
portfolio.html    Portfolio (currently placeholder tiles)
packages.html     Packages & pricing
about.html        About / bio
contact.html      Contact form (Formspree)
404.html          Custom not-found page
css/style.css     All styles
js/main.js        Mobile nav toggle
js/clarity.js     Microsoft Clarity user behaviour analytics
assets/img/       Logo + emblem, portfolio photos
```

## Before you launch: things to fill in

Search the codebase for these and replace them:
- **`brianvalachovic@gmail.com`** — used as a placeholder contact email in the footer of every page and on `contact.html`. Swap for a dedicated business email if/when you set one up.
- **`[Your Name]`** and the bio paragraphs in `about.html` — replace with your actual story.
- **Portfolio tiles in `portfolio.html`** — each `.portfolio-placeholder` div should become a real `<img>` once you have photos of finished pieces. There's a comment at the top of the gallery in that file with exact instructions.
- **Pricing in `packages.html`** — all dollar amounts are examples. Update to your real rates.
- Social links (e.g. Instagram) — there's a commented-out example block in `contact.html`'s sidebar ready to uncomment once you have a handle to link.

## Formspree setup (contact form)

1. Create a free account at [formspree.io](https://formspree.io).
2. Create a new form pointed at whatever email should receive inquiries.
3. Copy the endpoint it gives you (looks like `https://formspree.io/f/xxxxabcd`).
4. Paste it into the `action` attribute of the `<form>` in `contact.html`, replacing `YOUR_FORM_ID`.
5. Once deployed, submit one test message from the live site — Formspree requires a confirmed first submission before it starts forwarding to your inbox.

Free tier covers 50 submissions/month, which is plenty for word-of-mouth traffic.

## Deploying to GitHub Pages

You mentioned wanting the site at `tenderviolet.github.io` — a couple of things worth knowing about that:

- A URL of the exact form `<name>.github.io` is a **user/org "root" page**, not a regular project page. To get it, the repository itself must be named **exactly** `tenderviolet.github.io`, and it must live under a GitHub account or organization named `tenderviolet`. If your GitHub username isn't `tenderviolet`, you'd need to create a separate account/org with that name (GitHub allows one free org per person without extra cost) and push this repo there.
- If that's more than you want to deal with right now, the simpler path is a normal **project page**: push this repo under your existing account with any name (e.g. `tender-violet-studio`), and it'll be served at `https://<your-username>.github.io/tender-violet-studio/`. You can move to a custom domain (`tendervioletstudio.com` or the root `.github.io` above) later without losing any work — the file structure doesn't change either way.

### Steps (once you know which path you're taking)

1. Push this repo to GitHub under the account/org and repo name you've decided on.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save — GitHub will publish the site at the corresponding URL within a minute or two.
5. If you later buy a custom domain, add a `CNAME` file to the repo root containing just the domain name, and point your DNS at GitHub's Pages IPs (GitHub's Pages docs walk through the exact records).

## Local preview

No build tools needed — just open `index.html` in a browser, or serve the folder with any static file server, e.g.:

```bash
npx serve .
```
