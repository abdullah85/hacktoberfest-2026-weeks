# Week 2: Side Hustle — SpotWise

The `spotwise` project, my entry for https://dev.to/challenges/hacktoberfest-week2-2026-10-12

**SpotWise** is a precious-metals research and paper-trading web app.
Code repository: `spotwise`. Deadline: **19 Oct 2026, 12:29 PM IST**.

## Goal
Help a long-term saver plan gold, silver and platinum purchases and sales against real price history,
with every figure shown in their own currency and tax terms.

## Priorities
1. **Charts that work flawlessly.**
2. **AI as the standout feature:** research, backtesting and what-if scenarios, with results drawn on the chart.
3. Everything else is secondary.

## Scope
1. Charts for gold, silver and platinum
2. At least five years of daily history
3. Multiple currencies
4. User-defined tax details (duty, premium, GST or VAT) with effective dates
5. Buy and sell markers overlaid on the chart, with position and profit and loss

All calculations are plain, tested code. The interface is quick and uncluttered.

## Stack
- Frontend: React
- Backend: FastAPI (rates, backtest and what-if engines, AI endpoints)
- AI: open-weight model served on the backend, with a template-text fallback
- Data: metals.dev, credited as "Prices by metals.dev" on every screen that shows it

## AI layer
A language model turns what the user types into a structured request. Code runs it, and the model explains the result.
- **Research:** questions about past price behaviour
- **Backtesting:** strategies described in words, compared with plain monthly buying
- **What-if scenarios:** changes in metal price, currency or tax applied to the user's position
- **On-chart results:** a backtest draws its buys and sells next to the user's own trades

The model never does the arithmetic.

## Chart acceptance checklist
- [ ] Conversions match the tested formulas for every supported currency
- [ ] Switching currency keeps the selected date range
- [ ] Five years of data load fast, with zoom, pan and range buttons (1M, 6M, 1Y, 5Y, Max)
- [ ] Tooltip on every point; weekends and gaps handled
- [ ] Buy and sell markers sit on the correct dates
- [ ] Tax-inclusive toggle works and uses the rate in force on each date
- [ ] Gold, silver and platinum switch cleanly
- [ ] Works on a phone-width screen
- [ ] Clear empty, loading and error states

## Constraints
- The dataset and API keys are never committed to a repository
- No raw price-history download, and no resale or ownership claim over the data
- Not financial advice
- The code repository is new, started and finished inside the challenge window

## Milestones
- [ ] M1: data layer, charts, currencies, tax profiles
- [ ] M2: ledger with buy and sell overlay, profit and loss
- [ ] M3: backtest and what-if engines (tested)
- [ ] M4: AI layer with on-chart results
- [ ] M5: polish, demo recording, write-up, publish (aim to finish by 11:30 AM)

## Later
Sheets sync, alerts, payments, multi-device sync.
