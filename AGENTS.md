# Repository instructions

## Hugo toolchain

- This site uses the standard, non-extended Hugo `0.170.1` release, matching the GitHub Pages workflow.
- Use the repository-local `./.bin/hugo` executable instead of a globally installed `hugo` command.
- Confirm the toolchain before testing with `./.bin/hugo version`. The output must report `hugo v0.170.1`.
- Run a production-equivalent build with `./.bin/hugo --minify`. Hugo writes the generated site to `public/`; never edit or commit that directory.
- Start a local preview with `./.bin/hugo server --bind 127.0.0.1 --port 1313`.
- While the preview server is running, inspect a route with `curl -i http://127.0.0.1:1313/<path>`. For example, verify the crawler policy with `curl -i http://127.0.0.1:1313/robots.txt`.
- If `./.bin/hugo` is missing or reports a different version, download the standard archive for the host platform from the official [Hugo release](https://github.com/gohugoio/hugo/releases/tag/v0.170.1), verify it against the published checksums, and place the executable at `.bin/hugo`.
