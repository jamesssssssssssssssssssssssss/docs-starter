# VerifyYou at The Quirk's Event — microsite

A landing-first Mintlify site for The Quirk's Event, New York (July 29 and 30, 2026). A
market-research attendee scans a QR on a business card or LinkedIn, lands on the home page, and
finds the quick version: the problem in third-party numbers, how the check works, the white paper,
the one-pager, the market-research video, and a way to book time. Copy is in David's voice, every
fraud stat is attributed to its source, and the design matches the main verifyyou docs.

Live at **verify-you.mintlify.site**. Pushing to `main` redeploys automatically.

## Pages

- `index.mdx` — home (custom-mode landing, no sidebar), with the market-research video embedded
- `the-problem.mdx` — survey fraud in third-party numbers (NORC, Kantar, Greenbook)
- `how-it-works.mdx` — liveness and uniqueness, and the honest boundary
- `white-paper.mdx` — "The Human Data Premium"
- `one-pager.mdx` — the whole thing on one printable page
- `meet-us-at-quirks.mdx` — book time, ask about the dinner, grab the assets
- `docs.json` — config, `style.css` — house styling, `logo/`, `favicon.svg`

## Run locally

```bash
npm i -g mint        # requires Node >= 20.17
mint dev             # http://localhost:3000
```

## Still to confirm before the show

- White paper PDF download button points at `https://verifyyou.com/human-data-premium.pdf` — swap for the real hosted PDF or remove the button (the on-page version stands alone).
- Confirm Wes Michael is comfortable being named on a public page (dinner section), and the "40-year veteran" figure.
- The market-research video is Vimeo `1160337449`; if it is domain-restricted in Vimeo privacy settings, allow `verify-you.mintlify.site`.

## Rules baked in (do not undo by accident)

- No em-dashes or en-dashes, no corporate jargon (David's voice).
- Every fraud number is attributed to NORC, Kantar, or Greenbook, framed as a third-party figure, never a VerifyYou measurement.
- Never call VerifyYou "identity verification" or "KYC" except to say it is not that.
- No customer-specific proof point on any public page.
- Booking CTAs point to `https://sales.verifyyou.com/`; the dinner asks stay as email on purpose.
