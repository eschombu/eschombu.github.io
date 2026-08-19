# erikschomburg.com

Personal site. Jekyll, hosted on GitHub Pages, served at
<https://erikschomburg.com>.

**There is no build step on your machine.** GitHub builds the site server-side
when you push. You never need Ruby installed to update this site.

## Updating the site

```sh
# edit index.md or cv.md
git add -A
git commit -m "Update CV"
git push
```

Wait ~30–60 seconds and the change is live. Build status is under the repo's
**Actions** tab — a red X there means the site didn't rebuild and the old
version is still being served.

You can also edit files directly on github.com if you're away from your laptop.

## Layout

| Path                      | What it is                                        |
| ------------------------- | ------------------------------------------------- |
| `index.md`                | Landing page                                      |
| `cv.md`                   | CV page                                           |
| `_config.yml`             | Site title, profile links, email                  |
| `_layouts/default.html`   | The HTML shell every page is poured into          |
| `assets/css/style.css`    | All styling; design tokens at the top             |
| `assets/favicon.svg`      | Tab icon                                          |
| `CNAME`                   | Tells GitHub Pages the custom domain. Don't delete. |

Pages appear in the nav automatically if their front matter has a `nav_order`.

## Changing how it looks

Everything is driven by the custom properties at the top of
`assets/css/style.css` — colors, fonts, and the two width variables. Both a
light and a dark palette are defined; the site follows the visitor's system
setting. Change `--accent` first if you want a different feel.

## Adding a blog later

Jekyll gives you this nearly for free when you want it:

1. Make a `_posts/` directory, add `2026-08-19-my-first-post.md` with front
   matter `layout: default` and a `title`.
2. Create `writing.md` with `nav_order: 3` that loops over `site.posts`.

Ask me and I'll wire it up.

## Local preview (optional)

Not required, and it's the one place Ruby enters the picture. If you want it,
install Ruby via a version manager and keep the gems project-local:

```sh
bundle config set --local path vendor/bundle   # gems go in ./vendor, gitignored
bundle install
bundle exec jekyll serve                       # http://localhost:4000
```

This needs a `Gemfile` (`gem "github-pages", group: :jekyll_plugins`), which
isn't committed yet since nothing so far has needed it.

## Notes

- The email address in `_config.yml` is published on the landing page as a
  `mailto:` link, which means scrapers will find it. Delete the `email:` line
  to remove it.
- HTTPS is provided free by GitHub via Let's Encrypt and renews itself. Keep
  "Enforce HTTPS" checked in **Settings → Pages**.
- The repo must stay **public** for Pages to serve it on a free account.
