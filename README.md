# DI-Sports

DI-Sports is a Grounded DI public archive of structured NFL forecasts, probability conversions, entropy-based risk analysis, and dated sports-pick demonstrations.

**Published by:** Grounded DI LLC · **Creator / operator:** Mark S. Weinstein · **Public repository established:** August 1, 2025

## Overview

The repository preserves five dated forecast and strategy artifacts:

- NFL_Week_1_Eagles_Cowboys.md
- NFC_East_DI_Sports_2025-08-14.md
- NFL_Fantasy_Draft_Guide
- Eagles_Chiefs_9-14
- NFL_Week_2_Picks

They show how DI-Sports turns a matchup or fantasy brief into explicit assumptions, probability bands, entropy measures, pick rationale, and a stated review boundary. The materials are historical demonstrations and educational records. They are not current odds, a live feed, a wagering service, or a guarantee of forecast accuracy.

No executable forecasting model, data connector, dependency manifest, test suite, CI workflow, or current source archive is included. “Deterministic” is used narrowly for fixed calculations and stated rule paths under the inputs recorded in each artifact.

## Why It Matters

Sports analysis is vulnerable to hidden assumptions and compounded uncertainty. DI-Sports makes some of those assumptions visible: moneyline conversion, information entropy, support relationships between legs, and thresholds that flag a high-variance parlay. That structure gives a reviewer a clearer basis for inspecting a pick than an unexplained confidence label.

## Key Records

| Artifact | What the repository records | Status / boundary |
|---|---|---|
| NFL_Week_1_Eagles_Cowboys.md | August 1, 2025 pregame forecast for Eagles–Cowboys Week 1, including a predicted Eagles margin of 10–14 points and modeled outcome probabilities. | Historical forecast; not a recorded game result or independently scored prediction. |
| NFC_East_DI_Sports_2025-08-14.md | Division preview with logic-labeled team signals, win ranges, collapse-risk labels, and a final ranking. | Creator-authored preseason assessment; not a statistical benchmark or final-season record. |
| Eagles_Chiefs_9-14 | September 13, 2025 Eagles–Chiefs analysis with spread and total bands, support-entropy formulas, and an illustrative two-leg versus three-leg comparison. | Pregame analysis and educational risk lens; not wagering advice or a current line. |
| NFL_Week_2_Picks | A 16-game Week 2 lines snapshot citing ESPN, CBS Sports, and VegasInsider timestamps, with moneyline-implied probabilities and picks. | Time-bound snapshot; referenced source captures and the generated CSV/chart paths are not included in this repository. |
| NFL_Fantasy_Draft_Guide | 2025 fantasy draft tiers, player notes, Entropy Risk Scores, trap labels, and draft-day prompts. | Educational strategy guide; player status and projections are not continuously updated or independently benchmarked. |

## What the Record Demonstrates

### Fixed probability and entropy calculations

The Eagles–Chiefs analysis defines the moneyline conversion:

- Negative odds: p = |odds| / (|odds| + 100)
- Positive odds: p = 100 / (odds + 100)

It then defines information entropy per leg as H = −log₂(p). Lower H indicates a higher implied probability under the stated line; it does not measure actual team quality or guarantee an outcome.

### Support-entropy risk lens

The same record defines:

- Parlay Entropy Score (PES): sum of leg entropies less pairwise correlation credits.
- Support Entropy (SE): conditional uncertainty added by a supporting leg.
- Support Integrity (SI): 1 − H(S|T) / H(S).

Its stated thresholds classify PES ≤ 1.5 as low entropy, 1.5–2.5 as medium, and values above 2.5 as flagged. The illustrative core duo is scored around PES 1.56–1.64; adding a player leg is scored around 2.7–2.9 and flagged. These are calculations in the dated demonstration, not validated betting edges.

### Forecast records

The Week 1 file records 61% for an Eagles win by 7–14, 13% for an Eagles blowout, 17% for a Cowboys narrow win, 3% for a Cowboys blowout, and 6% for a tie or chaos outcome. The NFC East preview records win ranges of Eagles 11–13, Cowboys 8–12, Giants 6–9, and Commanders 4–7. These values remain visible as historical outputs of the archive.

## Technical Significance

The useful design pattern is the separation of a forecast thesis from its uncertainty accounting. A commercial evaluator could reuse the same structure with a versioned odds feed, source snapshots, model inputs, calibration records, and an explicit hold state for stale or conflicting data.

## Recorded Checks

| Check | Result | Evidence |
|---|---|---|
| Week 1 forecast | Eagles win by 10–14 points; probability rows sum to 100% in the artifact | NFL_Week_1_Eagles_Cowboys.md |
| NFC East preview | Four-team ranking with stated win ranges and collapse-risk labels | NFC_East_DI_Sports_2025-08-14.md |
| Support-entropy example | Core PES approximately 1.56–1.64; three-leg example approximately 2.7–2.9 and flagged | Eagles_Chiefs_9-14 |
| Week 2 lines snapshot | Sixteen matchups with cited timestamped lines and implied probabilities | NFL_Week_2_Picks |
| Fantasy strategy guide | Position tiers, Entropy Risk Scores, and trap labels recorded | NFL_Fantasy_Draft_Guide |
| Repository review during this update | Six tracked files inspected; no executable model, data feed, tests, dependencies, CI, or generated CSV/chart found | Current main tree and Git history |

The forecast and probability figures are artifact-recorded outputs. No independent accuracy assessment or live rerun was performed from this repository.

## Scope and Limitations

- Lines, injuries, rosters, schedules, and player roles are time-sensitive; the records are historical snapshots.
- The cited ESPN, CBS Sports, VegasInsider, and other source material is named in the artifacts but is not archived here for independent replay.
- Forecast probabilities are model or market-implied values in the records, not observed frequencies or guarantees.
- All sports and fantasy materials are educational and not wagering, financial, or professional betting advice.
- No production forecasting service, API, sportsbook integration, or benchmark corpus is included.
- No open-source license is present.

## How to Review

~~~bash
git clone https://github.com/Grounded-DI/DI-Sports.git
cd DI-Sports
~~~

Start with Eagles_Chiefs_9-14 for the entropy formulas and risk lens. Then review the Week 1 forecast, the NFC East division map, the Week 2 lines snapshot, and the fantasy guide. For any current use, obtain fresh lines and source captures before calculating or publishing a pick.

## Evaluation and Integration Context

The archive can support a scoped proof of concept for dated sports analytics: ingest a versioned odds snapshot, calculate implied probability and entropy, preserve assumptions and source timestamps, flag compounded uncertainty, and route publication through human review.

A responsible pilot would add live-data provenance, historical backtesting, calibration, error reporting, responsible-gambling controls, and a correction path. Nothing here establishes a profitable strategy, customer adoption, or wagering authorization. Commercial licensing and integration inquiries: [Grounded DI GitHub organization](https://github.com/Grounded-DI).

## Authorship, Provenance, and Intellectual Property

Git history identifies Grounded DI LLC and Mark S. Weinstein as the repository authorship identity beginning August 1, 2025. The artifacts preserve their dates, formulas, source labels, probability tables, risk thresholds, and signal identifiers as public provenance records. These records support technical chronology and traceability; they do not independently establish forecast correctness, legal ownership, or patent priority.

No open-source license is present. Public availability does not grant reuse rights to the analyses, formulas, branding, or nonpublic implementation materials. Review any future license, notice, citation file, release tag, and filing reference separately with counsel.

## Status

**Status:** Active public sports-analysis and demonstration archive. It preserves historical NFL forecasts, fantasy strategy, and an explicit entropy-based risk framework; it is not a live sports-data product, certified forecasting system, or wagering service.

## Discovery

#DISports #SportsAnalytics #Forecasting #Reproducibility #EntropyAnalysis #AuditTrail #ResponsibleAI #GroundedDI
