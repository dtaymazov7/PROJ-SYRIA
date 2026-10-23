# Handoff: Syria solar idea, session of 2026-10-22

Start here. This summarizes a Claude Code session so work can continue in Cowork. The two working files are:

- `docs/designs/syria-solar-lease-to-own.md`: approved design doc (the decision record).
- `models/lease-to-own-unit-economics.xlsx`: scenario model. Switch scenarios in `Assumptions!C4` (1 Base, 2 Bad, 3 Good).

Also relevant: the **Microgrid YC Validation Pack** Claude Doc (https://claude.ai/artifact/D2RuF84PCFUYQYCRKxJUFk), which holds the earlier 15-year power-as-a-service plan, sanctions research, competitor map, interview script and YC application drafts.

## Where things stand

- **Decision:** pursue 36-month lease-to-own solar financing for Aleppo factories (al-Kalasa, al-Arqoub), entered through partner-only cash sales. The 15-year power-as-a-service plan in the Validation Pack is dropped.
- **Stage:** pre-product. No interviews, no LOIs, no named customer, no Aleppo partner, no founder in Syria.
- **Next action (the assignment):** by 2026-11-05, get one Aleppo factory owner to send a photo of last month's diesel invoice, through one named connector. Put the real numbers into the model.

## Key numbers (base case, 100 kWp + 100 kWh system)

| Item | Value |
|---|---|
| Landed cost / price to factory | $83.4k / $90.1k (cost + 8%) |
| Deposit / capital out per deal | 25% ($22.5k) / $60.9k |
| Monthly lease payment | $2,794 for 36 months at 28%/yr, USD-indexed |
| Factory's diesel avoided / net saving during lease | $58.1k / +$24.6k per year |
| Financier IRR / NPV at 25% | 28.1% / +$2.1k (about +$0.9k once years 2-3 of insurance are counted) |
| Bad case | 13.0% IRR, -$10.0k NPV, and the factory loses money |
| Payback month (cumulative cash positive) | 26 |
| $500k pilot pool | about 33 deals over 5 years |

The go/no-go variable is the share of solar output that replaces diesel rather than grid power. It must be at least about 60%. That depends on whether the factory's ~12 grid hours fall during working hours.

## How we got here

1. **Council deliberation** (Munger, Machiavelli, Sun Tzu). All three said the hardware is easy and the real business is collecting payment, permits and local trust. All three said to pilot small (under $500k, survivable as a total loss) with productive-use customers and to avoid neighbourhood microgrids. The council split on ownership: Munger and Sun Tzu preferred supplying or financing installers over owning assets in someone else's territory; Machiavelli argued that just swaps seizure risk for credit risk. Added tests: 3-5 sign-up conversations before any capex, and a pre-set walk-away trigger if a state or Gulf-backed utility is licensed to serve the same area. The council stopped after Round 2 when the work moved to /office-hours.
2. **/office-hours diagnostic.** Asked for demand evidence, the status quo and a named customer, the founder answered "None yet", "Don't know yet" and "Nobody yet".
3. **Landscape research** (via Aside, Oct 2026). Findings that changed the plan:
   - Africa GreenTec, the Validation Pack's "closest model", entered preliminary insolvency on 3 June 2026 ([ecoreporter](https://www.ecoreporter.de/artikel/africa-greentec-ist-insolvent/)).
   - ecoligo missed investor payments in 2026 after customer arrears; its lender expects about 60% recovery ([test.de](https://www.test.de/Crowdfunding-Aerger-um-verspaetete-Zahlungen-bei-Ecoligo-6301435-0/)).
   - Syrian factories already lead rooftop solar adoption and pay cash; no pay-per-kWh solar found in the region ([The National](https://www.thenationalnews.com/business/energy/2026/07/06/syrias-solar-boom-is-redefining-middle-easts-energy-model/), [People in Need](https://www.peopleinneed.net/the-growing-business-of-solar-power-in-northern-syria-and-what-it-needs-to-function-better-13740gp)).
   - Lebanon's SoLR& fund does donor-backed lease-to-own for small businesses, ownership after 5-7 years ([Arab Reform](https://www.arab-reform.net/publication/unlocking-solar-energy-access-in-lebanon-through-innovative-finance-and-blended-models/)).
   - Known killers in fragile markets: cash collected in person, free power at launch, grid arrival (80-90% customer loss), dollar contracts during devaluation ([IGC toolkit](https://www.theigc.org/sites/default/files/2024-09/Mahmood%20Policy%20toolkit%20September%202024.pdf)).
4. **Insight:** the gap isn't "nobody sells power-as-a-service in Syria". It's that nobody finances the factories that want solar but can't pay $50k-100k upfront. Short leases carry far less risk than 15-year contracts.
5. **Approaches compared:** A, 15-year power-as-a-service (16% IRR, below the 25% hurdle, rejected); B, 36-month lease-to-own (recommended); C, cash installer (used as phase 1 of B).
6. **Design doc review:** independent spec review passed after 3 rounds (6, then 7, then 8 out of 10). The 13 remaining minor notes were then fixed in the text but not re-reviewed.

## Plan in the design doc

- **Gate 0** (target 2027-01-31): a named Aleppo installer partner signed up; 20 interviews and one LOI; a sanctions lawyer has classified every bill-of-materials item as exportable. Quotes are allowed before Gate 0; purchase orders, payments and shipments are not.
- **Phase 1** (~3 months after Gate 0): partner-only cash sales, no company inventory or capex. Log grid hours, generator hours and diesel litres at every factory visit; one-week load loggers at shortlisted factories.
- **Phase 2** (months 3-12): leases only to factories passing the entry gate (invoice-based diesel data, at least 60% displacement, at least 20% net saving, legal opinion on repossession). A founder must be in Aleppo before the first lease.
- **Then:** raise development-lender debt after 12 months of repayment data.

## Open questions

- Do al-Kalasa factories run their own generators, buy from ampere operators, or already have panels?
- Will owners accept USD-indexed payments, and how do they pay for diesel today?
- Who is the Aleppo partner, and which founder goes to Syria, when?
- Are the lease and repossession enforceable in Aleppo?
- Which development lender or donor facility would back a Syria pilot pool?

## Known gaps and caveats

- All cost and diesel figures are desk estimates from the Validation Pack; none are verified.
- Insurance for years 2-3 of the lease is not in the model (the design doc notes the NPV effect).
- The workbook was checked with a Python formula engine, not Excel or LibreOffice; open it once in Excel or Numbers to confirm it recalculates.
- The 13 minor fixes in the design doc were not re-reviewed.

## Suggested opening prompt for Cowork

> Read docs/HANDOFF.md and docs/designs/syria-solar-lease-to-own.md. Then help me with The Assignment: finding one Aleppo connector and getting a diesel invoice by 2026-11-05.
