# Jumpstart site

A small multi-page Jekyll site served by GitHub Pages at the repository root.
Content lives in `index.md`, `going-further.md`, `how-to-study.md` and
`help.md`; the look lives in `_layouts/default.html` and `assets/site.css`.
There is no theme and no plugin, so GitHub Pages builds it with nothing beyond
this repository.

`index.md` is the only page that carries a year. The other three are written to
be reused each September; keep cohort-specific material off them.

## Editing

- **Adding a page.** Create `name.md` with `layout: default`, a `title`, a
  `description`, and `permalink: /name/` (trailing slash, so the URL is a
  directory). Then add a matching entry to `_data/nav.yml`.
- **Header navigation.** Comes from `_data/nav.yml`, one `{url, label}` per
  page, and appears on every page. The `url` must match that page's
  `permalink` exactly, trailing slash included, or the current page will not be
  marked and nothing will warn you. Do not write the `baseurl` into
  `_data/nav.yml`; the layout adds it with `relative_url`.
- **Within-page navigation.** Each `##` heading can carry an explicit id,
  `## Title {#id}`. Listing the id and a short label under `sections:` in the
  page's front matter renders a secondary bar under the header. Pages without a
  `sections:` list have no bar. This drives the *within-page* bar only; page
  links come from `_data/nav.yml`.
- **Placeholders.** A paragraph followed by `{: .placeholder}` renders as an
  amber "to fill in" box.
- **Sources.** A paragraph followed by `{: .source}` renders as a muted,
  rule-bordered citation line. Use it to close a write-up.
- **Reading lists.** `<ul class="reading">` with `<a>` title, `<span class="src">`
  source, and a `<p>` saying what the item is for. Write the contents as plain
  HTML: kramdown does not process Markdown inside block-level HTML, though
  Liquid still runs, so `relative_url` works inside.
- **Downloads.** Put files in `files/` and link them with
  `{{ '/files/name.pdf' | relative_url }}` so the link survives a `baseurl`.
  `files/` is currently empty; a download link to a missing file 404s with no
  build error.
- **Footer.** `contact:` in `_config.yml` adds a contact line. The "Updated"
  date is the build date of the whole site, not of the page you are reading.

## Local preview

Needs Ruby 3 or newer. The macOS system Ruby is 2.6 and will not do. Install
one first, then preview:

```
brew install ruby
export PATH=/opt/homebrew/opt/ruby/bin:$PATH
ruby -v                                  # must print 3.x

bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve --livereload
```

Then open **http://127.0.0.1:4000/JumpStart/**, not the server root. `baseurl`
is `/JumpStart`, and Jekyll's development server mounts the site under it; the
root returns 404 and looks like a broken build.

GitHub Pages builds with Jekyll 3.10 rather than the Jekyll 4 in the Gemfile;
the site uses no feature that differs.

## Before pushing

```
grep -rn 'href="/\|src="/\|href="assets\|href="files' _layouts *.md   # want no output
grep -n '](#' *.md                                                    # stale fragments
bundle exec jekyll build
grep -o 'href="[^"]*"' _site/*/index.html _site/index.html | grep -v 'http'
```

Every internal href in that last list must begin `/JumpStart/`. Then walk the
pages and confirm exactly one header link carries the red underline on each.

## Deploying

In the repository settings, under Pages > Build and deployment, choose
Source: *Deploy from a branch*, branch `main`, folder `/ (root)`. GitHub runs
Jekyll on every push.

If the site is served at `https://<user>.github.io/<repo>/`, set
`baseurl: "/<repo>"` in `_config.yml`. Leave it empty for a custom domain or a
`<user>.github.io` repository. The path is case-sensitive:
`gsathish.github.io/jumpstart/` is a 404.
