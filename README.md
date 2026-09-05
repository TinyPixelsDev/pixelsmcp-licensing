# pixelsmcp-licensing

Public infrastructure for [PixelsMCP](https://github.com/TinyPixelsDev/PixelsMCP) licensing.

- **`revocations.pxrl`** — a signed list of revoked licence ids. The plugin polls this URL
  (`Revocation List Source` setting) and refuses any licence whose id appears here. Contains
  only hashes and a signature — no personal data, no keys. Safe to be public.
- **`docs/`** — the pricing page (Stripe Pricing Table embed), served via GitHub Pages.

Nothing sensitive lives in this repo. Signing keys and issued-licence records are kept
offline/private, never committed anywhere — see the plugin's `_LicenseAuthority` notes.
