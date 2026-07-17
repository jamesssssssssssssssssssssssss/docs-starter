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
- `white-paper.mdx` — "The Human Data Premium": a readable web version plus a download card
  (cover preview at `images/wp-cover.jpg`) for the full designed PDF at
  `https://verifyyou.com/assets/pdfs/mr-white-paper.pdf`
- `one-pager.mdx` — the whole thing on one printable page
- `meet-us-at-quirks.mdx` — book time, ask about the dinner, grab the assets
- `docs.json` — config, `style.css` — house styling, `logo/`, `favicon.svg`

## Run locally

```bash
npm i -g mint        # requires Node >= 20.17
mint dev             # http://localhost:3000
```

## Still to confirm before the show

- The white paper PDF is now wired to the real hosted file (`verifyyou.com/assets/pdfs/mr-white-paper.pdf`). The host serves it `content-disposition: inline`, so it opens in the browser viewer; set it to `attachment` on the host if you want the button to force a save instead.
- The hero is a local muted-autoplay clip of Wes Michael (`videos/sizzle-hero.mp4`), credited "President and Founder of Rare Patient Voice, now part of Konovo", with two supporting clips on the Why VerifyYou page. The clip notes (`QUIRKS_WES_VIDEO_CLIPS.md`) say to confirm the final cut with Wes before it goes public under his name and face.
- The market-research explainer on The problem is Vimeo `1160337449`; if it is domain-restricted, allow `verify-you.mintlify.site`.

## Rules baked in (do not undo by accident)

- No em-dashes or en-dashes, no corporate jargon (David's voice).
- Every fraud number matches the white paper's figures and sources (Insights Association for the ~40%, Dartmouth/PNAS for the 99.8%, Imperva for the 51%, Kantar for discard rates, NORC for the industry range), framed as a third-party figure, never a VerifyYou measurement.
- Never call VerifyYou "identity verification" or "KYC" except to say it is not that.
- No customer-specific proof point on any public page.
- Booking CTAs point to `https://sales.verifyyou.com/`; the dinner asks stay as email on purpose.
