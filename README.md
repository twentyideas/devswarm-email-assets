# DevSwarm Email Assets

Publicly hosted images for DevSwarm marketing emails sent through PostHog.

This repo exists because email clients fetch images anonymously — Gmail proxies them
server-side through `googleusercontent.com` with no credentials — so every `<img src>`
in an email must be a public, absolute `https` URL. PostHog does not host images for
pasted HTML, and the main product repo is private.

**This is deliberately separate from the product and the marketing site.** Nothing here
is part of devswarm.ai; do not point marketing pages at these URLs, and do not add
assets here that belong to the site.

## URLs

Files in `images/` are served by GitHub Pages:

```
https://twentyideas.github.io/devswarm-email-assets/images/<filename>
```

For example:

```
https://twentyideas.github.io/devswarm-email-assets/images/DevSwarmGuy.png
```

## Adding an asset

1. Drop the file in `images/`
2. Commit and push to `main`
3. Wait for the Pages deployment to finish (~1 minute), then verify the URL returns 200

## Rules

- **PNG, JPG or GIF only.** SVG does not render in Gmail, Outlook or Yahoo Mail.
- **Export at 2x** the display size — most mail clients render on high-DPI screens.
- **Anything committed here is public.** That is fine for email artwork, which is public
  the moment a campaign sends, but do not put anything else here.
