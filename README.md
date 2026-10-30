# National Erosion Index

**Which economies can weather the next ten years, and which are likely to erode first?**

A hobby model that scores 42 of the world's most consequential economies on the problems building at home, the financial cushion each has to absorb a shock, and the trouble it imports from trade partners.

> I'm not an economist. Economics is a subject I love to read about, and AI (Claude) made it possible to build and test a model of my own design. Feedback, pushback and better data are very welcome.

**Not investment advice.** The scores mix published data with my own judgement.

---

## Try it

| Page | What it does |
|---|---|
| [Erosion and Cushion Map](erosion-cushion-map.html) | A guided, six-section tour: the big picture, then each of the four groups of countries |
| [Erosion Calculator](erosion-calculator.html) | Pick a country (or add your own), move the sliders or enter real figures, and see how the score is built |

Both are single HTML files with no install and no server. Open them in any browser.

---

## The idea in one picture

Every country is judged on three questions:

1. **How much damage is building at home?** 17 risk factors, each scored 1 (robust) to 10 (critical).
2. **How much money does it have to absorb a shock?** Reserves, sovereign wealth funds and room to borrow.
3. **How much trouble does it import?** Spillover from trade partners in difficulty and, for euro members, from each other.

The map plots question 1 (across) against question 2 (up), which splits countries into four groups:

| | Thin cushion | Deep cushion |
|---|---|---|
| **Modest problems** | **Sound but uninsured**: a careful household with no emergency fund | **Fortresses**: steady income and healthy savings |
| **Serious problems** | **Exposed**: behind on the bills with no savings | **Cushioned but cracking**: big savings, but running up debts |

---

## What goes into the scores

Factors that can do damage fastest carry the most weight: **×3 lethal**, **×2 serious**, **×1 background**.

| Group | Factor | Weight |
|---|---|---|
| Money & debt | Public debt & military spending vs growth | ×3 |
| | Loose money (inflation, deficits, money creation) | ×3 |
| | External fragility (foreign-currency debt, pegs, current-account deficits, IMF reliance) | ×3 |
| | Asset bubbles | ×2 |
| | Private debt (household & company debt, and how fast it is growing) | ×2 |
| Politics, conflict & society | Political instability | ×3 |
| | War or conflict | ×3 |
| | Crime | ×2 |
| | Health & education spending | ×1 |
| | Household formation (too slow or too fast) | ×1 |
| Resources & climate | Energy, food & medicine security | ×2 |
| | Physical climate risk (floods, heat, sea level) | ×2 |
| | Climate transition risk (dependence on fossil fuels) | ×2 |
| | Pollution | ×1 |
| Trade & technology | Trade weakness | ×2 |
| | AI disruption exposure | ×2 |
| | AI capability gap | ×2 |

---

## How the score is calculated (v8)

1. **Weighted average** of the 17 scores (total weight 36).
2. **Blend** = 70% weighted average + 30% the single worst lethal or serious score, so one very bad problem can't be averaged away.
3. **Credit-boom amplifier**: if private debt scores 7+ and asset bubbles or loose money also score 7+, add 0.5 × (private debt − 6). Credit-financed bubbles turn price falls into debt spirals (Minsky, Fisher, Keen).
4. **Shock absorber**: the cushion is scored 1 to 10, the part held in global markets is cut by 40% for a crash, and the result lowers the score by up to 25%.
5. **Spillover**: for each trade partner, export share × how far the partner's score is above 4.5. Euro members also pick up spillover from each other, weighted by share of euro-area GDP.
6. **Final score** = home-grown score + spillover, capped at 10.

| Final score | Outlook |
|---|---|
| 7.0 or more | Erodes first |
| 5.5 to 6.99 | At risk |
| 4.0 to 5.49 | Muddles through |
| Below 4.0 | Succeeds |

An optional switch counts strategic stockpiles (oil, grain) and 25% of public pension funds as extra cushion. It's off by default.

---

## Does it work? A brief back-test

Each crisis country was scored at a date before its crisis, using figures published at the time:

| Case | Score | Outlook | Result |
|---|---|---|---|
| Argentina, end-1998 | 5.70 | At risk | Flagged |
| Greece, end-2007 | 5.99 | At risk | Flagged |
| USA, end-2006 | 5.63 | At risk | Flagged (missed until private debt was added) |

Caveats: there are only three cases and no peer group, so false alarms are untested, and the scoring was done with hindsight.

---

## Data

- **As of:** 18 October 2026.
- **Sources:** IMF (World Economic Outlook, Fiscal Monitor, AI Preparedness Index), World Bank, BIS (private credit), UN World Population Prospects, ND-GAIN, Global Peace Index, Stanford AI Index and national statistics. Each source is listed with a link in the evidence table.
- **Judgement:** structural scores (crime, pollution, climate exposure and others) and the trade links rest on 2024–25 data and my own judgement.

---

## Known limits

- Spillover runs through trade only. Bank, remittance and capital-flow contagion are not modelled yet.
- Only partners within the 42 countries are counted.
- The weights, bands and cushion limits are a starting point, not calibrated on history.
- Help from outside (IMF programmes, allies, remittances) is not counted as a cushion.

---

## Feedback welcome

I'd especially value views on:

- Is the change in private debt the right signal, or should it be its acceleration (the credit impulse)?
- Would you weight any factors differently?
- What's missing?

Open an issue or message me on LinkedIn.

---

*Built as a hobby with the help of AI (Claude). Not investment, financial or policy advice.*
