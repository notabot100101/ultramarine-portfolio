# GA4 + consent banner for ultramarine963.com — ARMED, NOT YET MERGED

Analytics decision (Paul, 18 Oct 2026): GA4 installed on his word per site. Paul said "install GA4"
and gave this site's measurement id **G-LWTWQTB59S**, so `consent.js` is armed. It is still DARK
because this branch (claude/portfolio-ga4-consent) is UNMERGED; merge + deploy is the only go-live
action, and it waits for Lex's text. Design mirrors the trade site; the trade site goes first.

## What is built and armed
- `consent.js`: a bottom-of-page Accept / Decline banner that loads GA4 (gtag) ONLY after the visitor
  clicks Accept (TTDSG §25 + GDPR). Decline or ignore loads nothing. Choice stored in localStorage,
  not a cookie. `anonymize_ip` on, Google Signals / ad personalisation off. `GA4_ID` = G-LWTWQTB59S.

## Still to do before merge (Lex via the ads thread / board task #362, this site)
1. Replace the `[Lex: banner text]` string in `consent.js` with Lex's approved wording.
2. Add Lex's GA4 section to `datenschutz.html` with `id="analytics"` (matches the banner link).
3. Add `<script src="/consent.js" defer></script>` to the `<head>` of `index.html`, `impressum.html`
   and `datenschutz.html`, and reword the footer "Keine Cookies, kein Tracking" line on each.

Merge + deploy (branch hostinger-deploy auto-deploys) only after 1-3 are done. Paul's "install GA4"
armed the id; the merge is the install.
