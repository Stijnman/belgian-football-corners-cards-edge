---
name: belgian-football-corners-cards-edge
description: Generates high-edge singles and ACCAs for Belgian Pro League and Super Cup matches focused on corners and yellow cards. Trigger on Brugge Union tips, hoekschoppen, gele kaarten, Super Cup betting, or any Belgian football stats request for over corners cards goals.
---
# Belgian Football Corners & Cards Edge

## Instructions
1. Pull latest H2H, home/away corner averages, yellow card rates, and referee stats for the two teams.
2. Rank singles strictly by simulated hit rate. Prioritize:
   - Total corners over 7.5 / 8.5
   - Home team corners over 3.5 / 4.5
   - Away or underdog yellows over 1.5
   - Total yellows over 2.5
   - Over 1.5 goals and first-half over 0.5 goals as bankers
3. Build Safe ACCA (target hit rate ≥50 %, odds 1.90-2.20) using the top 4-5 highest-confidence legs only. Never include result markets in the Safe ACCA.
4. Build Balanced ACCA (odds 4.00-6.00) by adding one medium-confidence leg (BTTS or extra corner line).
5. Build High-risk ACCA only when requested and with explicit small-stake warning.
6. Output in exact Dutch structure:
   - Beste singles table (Rank / Selectie / Sim % / Waarom)
   - Vermijd list
   - Safe ACCA, Balanced ACCA, Value ACCA
   - Short 2- or 3-leg matrix
   - One-line conclusion stating corners + cards > result
7. Always state the match (teams + competition + kick-off) at the top.

## Failure Modes
- Missing recent corner or card data → fall back to season averages + H2H only and flag reduced confidence.
- Referee with extreme card profile → adjust yellow lines by ±0.5 and note it.
- Cup match or early season → lower all sim % by 5-8 points and warn.
- User requests exact score or clean sheet → reject and redirect to corners/cards.

## Success Criteria
- Safe ACCA contains only legs with sim ≥77 %.
- Output is copy-paste ready for a tipster channel.
- No result market appears in the recommended Safe ACCA.
- Corners and yellow cards dominate the ranking.

## When NOT to use
- Non-Belgian leagues.
- Requests focused purely on 1X2 or Asian handicaps.
- Live in-play after 60 minutes when corner data is already known.
