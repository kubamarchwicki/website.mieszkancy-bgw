# Repository instructions

## Hugo toolchain

- This site is pinned to the standard, non-extended Hugo `0.126.0` release for backward compatibility. Do not build or test it with another Hugo version.
- Use the repository-local `./.bin/hugo` executable instead of a globally installed `hugo` command.
- Confirm the toolchain before testing with `./.bin/hugo version`; the output must report `hugo v0.126.0`.
- Run a production-equivalent build with `./.bin/hugo --minify`. Hugo writes the generated site to `public/`; never edit or commit that directory.
- Start a local preview with `./.bin/hugo server --bind 127.0.0.1 --port 1313`.
- While the preview server is running, inspect a route with `curl -i http://127.0.0.1:1313/<path>`. For example, verify the crawler policy with `curl -i http://127.0.0.1:1313/robots.txt`.
- If `./.bin/hugo` is missing, download the standard Hugo `0.126.0` archive for the host platform from the official [Hugo release](https://github.com/gohugoio/hugo/releases/tag/v0.126.0), verify it against the published checksums, and place the executable at `.bin/hugo`.
