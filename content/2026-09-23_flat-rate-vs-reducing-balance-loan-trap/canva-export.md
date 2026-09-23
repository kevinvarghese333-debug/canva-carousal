# Canva export log — Flat rate vs reducing balance loan trap carousel

Canva editable design: 2026-09-23_flat-rate-vs-reducing-balance-loan-trap_carousel
Design ID: DAHWACwZg0E
Edit link: https://www.canva.com/d/SCun9MFQ6MZNYmV
Canva folder: @whenkevintalks Carousels / 2026-09-23_flat-rate-vs-reducing-balance-loan-trap

## Status

Built a new 9-page editable design this run (copied from the closest approved
style, the 2026-09-02 ULIP carousel, then rewrote every page's text and
recolored one slide from red to muted green for the brand's "upside" beat).
The design was reviewed page-by-page against the brand's design-quality
checklist (strong cover hook, distinct job per slide, off-white/navy
rhythm, gold-detail navy slide, minimal reveal slide, mechanism/proof
slide, red used once, green used once, no em dashes, slide labels and
handle present throughout) and passed.

1. Ran the `export-design` PNG job (1080x1350, pro quality, lossless) for
   all 9 pages: job succeeded, 9 signed download URLs returned.
2. Attempted to download the PNGs directly into this repo to build the ZIP
   and contact sheet.
3. Attempted `upload-asset-from-url` so Canva's own backend (not this
   sandbox) would fetch one exported PNG and store it as an asset in the
   Canva folder, as a workaround.

## Limitation hit (same as the 2026-09-22 run, not a Canva failure)

- This session's outbound network is filtered by an org egress proxy that
  rejects `export-download.canva.com` (confirmed via the proxy's own status
  endpoint: `connect_rejected`, "gateway answered 403 to CONNECT"), so the
  PNGs could not be downloaded directly into this repo.
- `upload-asset-from-url` was tried against the page 1 export URL as a
  workaround; it failed with `fetch_failed` ("HTTP response status code
  returned by the given URL wasn't 200"), the same failure Canva's own
  backend hit in the prior run — its export download links appear to be
  single-use/session-bound and cannot be re-fetched by a separate Canva
  job. Since this reproduces the exact documented failure mode from
  2026-09-22, the remaining 8 URLs were not retried individually.
- Net effect: the editable 9-page design is complete, on-brand, and saved
  in Canva. The export job itself succeeds. The individual PNG files and
  the ZIP could not be persisted to the Canva folder or to this repo from
  this session. This is an environment/network constraint on this session,
  not a defect in the design or the export.
- The design can be opened at the edit link above and exported to PNG
  directly from the Canva UI (Share > Download > PNG, all pages) by
  someone with browser access, which does not go through this session's
  egress proxy.

## Design quality check

- Slide 1 is a strong scroll-stopping hook (a specific, misleading rate
  vs. its real cost).
- Every slide has a distinct job matching the 9-slide rhythm: cover,
  problem, setup, mechanism/bar-comparison, worked example, minimal reveal,
  upside, rule/checklist, CTA.
- Off-white and navy backgrounds alternate (4 off-white: pages 2, 5, 7, 8;
  5 navy: pages 1, 3, 4, 6, 9); page 2's headline is huge navy type on
  off-white, satisfying that specific brand requirement; page 4 is the
  navy slide with a gold-bordered detail block; page 3 and page 6 are the
  deliberately minimal slides; page 4/5 carry the mechanism and worked
  proof.
- Gold used for labels/emphasis only; red used once (the "70 to 100% more"
  interest-cost reveal on slide 6); green used once (the "upside" slide 7,
  recolored from the template's red to the brand's muted green since this
  slide's message is positive, not a warning).
- Slide labels (01/09 ... 09/09) and @whenkevintalks present and
  unobtrusive on every page.
- No em dashes in visible copy.
- All key lines are legible at mobile scale in the thumbnails reviewed
  during editing.

## Notes

- Fonts are inherited unchanged from the copied ULIP template (no font
  edits were made), consistent with the established Instrument
  Serif/Manrope-style brand pairing used across this account's prior
  carousels.
