# Research notes: mutual fund expense ratio trap

## Why this topic
Existing @whenkevintalks carousels have covered lending traps (no-cost EMI,
flat-rate vs reducing-balance loans), credit traps (on-time credit card
trap, RBI weekly credit reporting), banking fees (minimum balance
penalty), salary fine print (CTC vs take-home), insurance-as-investment
(ULIP) and speculative trading (F&O trading trap), but nothing yet in the
"investing" bucket. Expense ratio is a strong next entry: it is a fee
every mutual fund investor pays but almost nobody checks, it does not
require citing a live regulation or a specific fund house, and it gives a
clean built-in visual contrast (two funds, same market, same 20 years,
different outcome because of one small percentage).

## Core facts used (kept generic/illustrative, not attributed to a specific fund)
- Expense ratio is the annual fee a mutual fund charges, expressed as a
  percentage of assets under management, deducted continuously from the
  fund's NAV rather than billed separately.
- It is charged every year the money stays invested, so its effect
  compounds alongside returns rather than being a one-time cost.
- A lower expense ratio does not by itself signal a worse fund; passively
  managed index funds typically carry materially lower expense ratios
  than actively managed funds.

## Worked example (own calculation, explicitly illustrative)
Monthly SIP of ₹10,000 for 20 years (240 months), assuming the same
illustrative 12% gross annual market return for both funds, compared at
two expense ratios:
- 0.5% expense ratio (11.5% net annual return): corpus ≈ ₹86.6 lakh
- 1.5% expense ratio (10.5% net annual return): corpus ≈ ₹76.8 lakh
- Total invested over the period: ₹24 lakh
- Gap caused purely by the 1-percentage-point fee difference: ≈ ₹9.77 lakh

Calculated using the standard SIP future-value formula,
FV = P × [((1+r)^n − 1) / r] × (1+r), with monthly rate r derived from
each annual net return and n = 240 months. Verified by direct computation
(not sourced from a third-party calculator).

## Why the framing avoids over-claiming
- The 12% gross return, and both expense ratios, are stated as an
  illustrative assumption for a worked example, not a promise or forecast
  about any specific fund's future performance.
- No specific fund, AMC, or regulator (e.g. SEBI expense ratio caps) is
  named or cited, so no time-sensitive regulatory figure is at risk of
  going stale.
- The takeaway is a general principle (compare fees, not just past
  returns) rather than a claim that any single number applies universally.

## Sources consulted
General knowledge of standard mutual fund expense ratio mechanics and SIP
compounding mathematics. The worked example numbers were computed directly
(Python, standard SIP future-value formula) rather than pulled from an
external source, so no external web research was required to keep the
content accurate.
