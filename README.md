# Jumpstart site

A single-page Jekyll site served by GitHub Pages at the repository root.
Content lives in `index.md`; the look lives in `_layouts/default.html` and
`assets/site.css`. There is no theme and no plugin, so GitHub Pages builds it
with nothing beyond this repository.

## Editing

- **Sections.** Each `##` heading in `index.md` is a section. Give it an
  explicit id, `## Title {#id}`, and list the id and a short label under
  `sections:` in the front matter; the header navigation is generated from
  that list and is hidden while the list is absent.
- **Placeholders.** A paragraph followed by `{: .placeholder}` renders as an
  amber "to fill in" box.
- **Downloads.** Put files in `files/` and link them with
  `{{ '/files/name.pdf' | relative_url }}` so the link survives a `baseurl`.
- **Footer.** `contact:` in `_config.yml` adds a contact line. The "Updated"
  date is the build date.

## Local preview

Needs Ruby 3 or newer. The macOS system Ruby is 2.6 and will not do; the
Homebrew one at `/opt/homebrew/opt/ruby/bin` works.

```
export PATH=/opt/homebrew/opt/ruby/bin:$PATH
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve --livereload
```

Then open http://127.0.0.1:4000/. GitHub Pages builds with Jekyll 3.10 rather
than the Jekyll 4 in the Gemfile; the site uses no feature that differs.

## Deploying

In the repository settings, under Pages > Build and deployment, choose
Source: *Deploy from a branch*, branch `main`, folder `/ (root)`. GitHub runs
Jekyll on every push.

If the site is served at `https://<user>.github.io/<repo>/`, set
`baseurl: "/<repo>"` in `_config.yml`. Leave it empty for a custom domain or a
`<user>.github.io` repository.
