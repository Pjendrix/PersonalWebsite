# Personal Website — Kryštof Benka

Single-page portfolio hosted on Firebase Hosting.

## Structure

```
index.html                  the entire site (markup, CSS, JS inline)
assets/
  img/       avatar.webp    profile photo
  logos/                    employer, university & certification logos
  watermarks/               decorative Czech landmark line icons
  icons/                    favicons & apple-touch-icon
firebase.json               hosting config (caching headers, clean URLs)
robots.txt, sitemap.xml     SEO
```

## Local preview

    python3 -m http.server 8000

Then open http://localhost:8000

## Deploy

    firebase deploy --only hosting

## Conventions

- **Images are WebP**, already resized to their display size. Resize before committing — don't ship a 1024px file for a 190px slot.
- **Filenames are descriptive**, lowercase, hyphenated (`rewe-group.webp`, not `asset_14.webp`).
- Adding a job or school? Drop the logo in `assets/logos/` and reference it with `loading="lazy" decoding="async"`.
- Country flags in Education load from flagcdn.com (external, not in repo).

## Notes

- The contact form posts to Formspree (`xwvjgqav`) and includes a `_gotcha` honeypot field.
- The aquarium/bubble section in "About Me" is intentionally complex — avoid refactoring it.
