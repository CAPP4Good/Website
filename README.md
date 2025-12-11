# CAPP 4 Good Website

Hugo static site. The repo includes the editable Hugo sources and the generated `public` output.

## Project layout
- `hugo.toml`: Site configuration (title, base URL, theme, languages).
- `content/en/_index.md`: Homepage content
- `content/en/about/index.md`: About page content folder (can include images or sub-sections).
- `content/en/post/`: Blog section; `_index.md` controls listing, individual `post_*.md` files are posts.
- `archetypes/default.md`: Front matter template used when running `hugo new`.
- `themes/ananke/`: Ananke theme assets/layouts; customize here if you need design changes beyond content.
- `public/`: Generated site output (overwritten by `hugo`); do not edit by hand.

## Run and develop
Run these commands in your terminal after cloning:

```sh
# Install Hugo Extended and Go (follow https://gohugo.io/installation/ if you need platform specifics)
# macOS example:
brew install hugo go

# From the repo root, download the theme module
hugo mod vendor

# Start the dev server with drafts (use a different port if 1313 is taken)
hugo server -D --bind 127.0.0.1 --port 1313

# Build the static site for production (outputs to public/)
hugo
```

Edit content under `content/en/`. Add a post with:
```sh
hugo new post/post_slug.md
```
