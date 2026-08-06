# SUNY Poly AI FYE

<https://sunypoly-com216-fall26.github.io/>

Course site for the AI-focused first-year experience pairing **FYS 111** with
**COM 216**.

## Editing the site

Edit a file, commit, push to `main`. GitHub rebuilds and republishes
automatically, usually within a minute. You do not need to run a build, and
there is no generated output in this repository.

Content lives in `_tabs3/` (the front-page tabs) and `index.html` (the page
itself). See **[SETUP.md](SETUP.md)** for the full guide, including optional
local preview.

## How it builds

`.github/workflows/build.yml` builds with Jekyll 4 on Ruby 3.4 and deploys to
GitHub Pages. Ruby and gem versions are pinned in `.ruby-version` and
`Gemfile.lock`.
