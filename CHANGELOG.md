# Changelog

## v2.1 — 2026-11-16

- **Compare mode** (CLI): one plan shape across several assets in a single run — `--compare SOL:150:60:250,ETH:3000:1500:6000` prints average cost, total size and value / P&L / return at each asset's target, side by side
- Unit tests: 12 cases (3 new covering compare parsing and row math)

## v2.0 — 2026-11-05

- **Backtest mode**: walk any staged plan through 1,000 days of real SOL daily closes (2024-02 → 2026-11, Binance public data baked into `data/sol-daily.json`)
- Start-date presets (cycle top / mid-range / crash), ladder depth −30% / −50% / −70%, all weighting modes
- Equity-vs-price chart with fill points; day-by-day fill table; all-in benchmark comparison
- **CSV export** of the plan table
- CLI backtest in `planner.py` (`--backtest --start … --depth …`)
- Unit tests: 9 cases covering ladder math, allocation, and the simulator (`tests/`)

## v1.0 — 2026-11-05

- Staged plan builder: geometric ladder, three weighting modes, running average cost
- Scenario table (value / P&L / return at key prices)
- Browser app (`index.html`) and CLI (`planner.py`)
