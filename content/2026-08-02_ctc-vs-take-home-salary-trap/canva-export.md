# Canva export log — CTC vs take-home carousel

Canva editable design: 2026-08-02_ctc-vs-take-home-salary-trap_carousel
Design ID: DAHRIJE-1Jc
Edit link: https://www.canva.com/d/GgMm9lk1yhC7XXP
Canva folder: @whenkevintalks Carousels / 2026-08-02_ctc-vs-take-home-salary-trap

## Status

The 9-page editable design already existed in Canva (built in a prior run) and
matches the approved draft copy, brand colours, slide labels (01/09-09/09) and
@whenkevintalks handle. This run:

1. Ran the design quality check (see below).
2. Exported all 9 pages as individual 1080x1350 PNGs via the Canva MCP
   `export-design` tool (job succeeded, 9 signed download URLs returned).
3. Exported a merged single-image contact sheet of all 9 pages (job succeeded).
4. Attempted to persist the PNGs back into the Canva folder (via
   `upload-asset-from-url`, which lets Canva's own backend fetch the export
   URL) and attempted to download them into this repo to zip them.

## Limitation hit (not a Canva failure)

- This session's outbound network is filtered by an org egress proxy that
  does not allow `export-download.canva.com` (confirmed via the proxy's own
  status endpoint: `connect_rejected`, "gateway answered 403 to CONNECT"),
  so the PNGs could not be downloaded directly into this repo to build the
  ZIP file.
- As a workaround, `upload-asset-from-url` was tried for all 9 exported PNGs
  so Canva's own backend (not this sandbox) would fetch them and store them
  as assets in the Canva folder. All 9 calls failed with `fetch_failed`
  ("HTTP response status code returned by the given URL wasn't 200") —
  Canva's export download links appear to be single-use/session-bound and
  could not be re-fetched by a separate Canva job.
- Net effect: the editable design and its 9 pages are complete and saved in
  Canva as required, and the export job itself succeeded, but the individual
  PNG files and the ZIP could not be persisted to the Canva folder or to this
  repo from this session. The signed export URLs below are valid for a few
  hours from generation (2026-09-22 ~06:42 UTC) and can be opened directly in
  a browser to download the 9 PNGs and the contact sheet manually, or the
  Canva "Download" button can be used from the edit link above.

## Design quality check

- First slide is a strong scroll-stopping hook (specific rupee figure vs. a
  broken promise).
- Every slide has a distinct job per the 9-slide rhythm (cover, problem,
  setup, mechanism/bar-comparison, worked example, reveal, upside, rule,
  CTA).
- Off-white and navy backgrounds alternate; gold used for labels/emphasis
  only; red used once (the "number you never receive" line) and green used
  once (the PF upside line), matching the "only when useful" rule.
- Slide labels (01/09 ... 09/09) and @whenkevintalks present, unobtrusive.
- No em dashes in visible copy.
- All key lines are legible at mobile scale in the thumbnails reviewed.

## Notes

- Fonts used in the existing design were not independently re-verified
  against the Instrument Serif / Manrope pairing in this run (no separate
  editing transaction was opened since no content edits were needed); the
  visual thumbnails show a serif/sans pairing consistent with the brand
  fallback.
