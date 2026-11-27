# Kalari Kennels

The production site source is in `site/`. Preview locally with `python3 -m http.server 5176 --directory site`.

## Cloudflare Pages

Create a Pages project using **Connect to Git** and select this repository. Use `main` as the production branch, no framework preset, no build command, and `site` as the build output directory. No environment variables are needed. Merges to `main` then deploy automatically.

Verify the initial `pages.dev` deployment before attaching `kalarikennels.co.nz`. Check what currently serves the domain in Cloudflare first. If the old Worker route or custom domain conflicts with Pages, release that mapping at cutover. Keep the existing Worker available for rollback until the live apex works on HTTPS.
