# Zero to Unicorn — public website

Static pages for App Store Connect (marketing, support, privacy, terms). Not a CMS.

## Host on Vercel

This is a static HTML/CSS site. Vercel can serve it as-is — no Next.js or build step.

1. Push this folder to GitHub (repo: `zerotounicorn`).
2. In [Vercel](https://vercel.com/new), import that repo.
3. Leave Framework Preset as **Other**, build command empty, output directory empty (or `.`).
4. Add the domain `zerotounicorn.com` under Project → Settings → Domains.

## Open locally

From this folder:

```bash
open index.html
```

Or serve the folder (cleaner for relative URLs):

```bash
python3 -m http.server 8080
```

Then visit [http://localhost:8080](http://localhost:8080).

## Before App Store submission

Replace every `https://apps.apple.com/app/idXXXXXXXXX` with the real App Store URL.

Search the site for `idXXXXXXXXX`.

If the live domain is not `zerotounicorn.com`, update origin copy and Open Graph URLs. Leave `contact@zerotounicorn.com` unless that mailbox changes.

## App Store Connect URLs

After this site is hosted at `https://zerotounicorn.com`:

```text
Marketing URL:  https://zerotounicorn.com/
Support URL:    https://zerotounicorn.com/support.html
Privacy URL:    https://zerotounicorn.com/privacy.html
Terms of Use:   https://zerotounicorn.com/terms.html
```

Email confirmation and password-reset links hand off to the iOS app from these pages (not linked in the public nav):

```text
Auth callback:  https://zerotounicorn.com/auth-callback.html
Password reset: https://zerotounicorn.com/auth-reset.html
```

## Files

- `index.html` — homepage
- `support.html` — support / FAQ
- `privacy.html` — privacy policy
- `terms.html` — terms & conditions
- `auth-callback.html` — email confirmation handoff to the iOS app
- `auth-reset.html` — password-reset handoff to the iOS app
- `styles.css` — shared styles
- `icon.png` / `favicon.png` — app icon
