# 1108 9th Avenue South — Edmonds, WA

Listing site for the new Schenkar Construction home at
1108 9th Avenue South, Edmonds, WA 98020.
Listed by **Adam E. Cobb**, Windermere Real Estate GH LLC — 206-854-9454.

---

## Putting it online

1. Create a new, empty repository on GitHub.
2. Upload **everything in this folder** — all the files, at the top level of
   the repo. `index.html` must end up in the repo root, not inside a folder.
3. In the repo, open **Settings → Pages**.
4. Under **Source**, choose **GitHub Actions**.
5. Wait about a minute. The address appears at the top of that same Pages
   settings screen.

That's it. There is nothing to edit, install or configure.

> **Uploading through the GitHub website?** Drag the *contents* of this
> folder into the upload box, not the folder itself. If you drop the folder,
> everything lands one level too deep and the site won't load.

### Why "GitHub Actions" and not "Deploy from a branch"

The site works either way. Choosing **GitHub Actions** additionally runs
`.github/workflows/deploy.yml`, which writes the live web address into the
page so that link previews — iMessage, Slack, Facebook, LinkedIn — show the
photo of the house. It also writes a `sitemap.xml` for search engines. You
never have to touch that file.

### Using a custom domain

Create a file named `CNAME` in the repo root containing only the domain:

```
1108ninth.com
```

Point the domain's DNS at GitHub Pages, then tick **Enforce HTTPS** in
Settings → Pages. The deploy workflow picks the new address up on its own.

---

## What's in here

| File | What it does |
| --- | --- |
| `index.html` | **The entire site.** Every photo, the floor plans, the styling and the scripts are inside this one file. |
| `og-image.jpg` | The photo shown when someone shares the link. Not used by the page itself. |
| `schenkar-development-onboarding.pdf` | The builder's onboarding one-pager, embedded in the Build Yours section. Keep this file — the embed points at it. |
| `404.html` | Shown if a visitor hits a bad link. |
| `favicon.svg`, `apple-touch-icon.png`, `icon-*.png` | The little icon in the browser tab and on phone home screens. |
| `site.webmanifest` | Lets the site be saved to a phone home screen. |
| `robots.txt` | Tells search engines they may index the site. |
| `.nojekyll` | Stops GitHub from trying to process the site as a blog. |
| `.github/workflows/deploy.yml` | Publishes the site and fills in the live address. |

The images are built into `index.html` on purpose. It means the page cannot
break because a file was missed, renamed or moved — if `index.html` is
there, the site is there.

---

## Editing

Everything is in `index.html`. Open it in any text editor and search for
what you want to change.

- **Price** — search `Price Upon Request`. It appears once.
- **Phone and email** — search `206-854-9454`.
- **Specifications** — the six blocks beginning `<article class="spec">`.
- **Colours** — the `:root` block near the top. `--paper` is the ivory
  background, `--ink` the text, `--crimson` the Schenkar red, `--gold` the
  accent. The `--img-*` values are the pale text sitting on top of the dark
  photo panels; leave those as they are.
- **Showing form** — `<form id="showform">`. Submitting it opens a
  pre-written email to `adamcobb@windermere.com`; there is no server
  involved, so there is nothing that can go down.

### Changing a photo

The photos are embedded as text (`data:image/jpeg;base64,...`), so they
can't be swapped by dropping in a new file. Ask for a rebuild with the new
photography and you'll get a fresh `index.html`.

---

## Notes

Renderings and floor plans are artist's and architect's representations.
Floor plans by H2D Architecture + Design. Dimensions, square footages and
finishes are approximate and subject to change during construction.
Equal Housing Opportunity.
