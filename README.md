# qb-banking · Bank of America Edition

A complete UI/UX redesign of [qb-banking](https://github.com/qbcore-framework/qb-banking) themed around **Bank of America**. Drop-in replacement — all backend logic, NUI callbacks, and database schemas are preserved exactly. Only the frontend (`html/`) was rewritten.

> **Pairs perfectly with** [**MrHunter · Bank of America MLO**](https://mrhunter.tebex.io/package/5063501) by **MrHunter** — drop the MLO into your map and this UI on top of qb-banking for a fully-themed banking experience.

---

## Highlights

- **Authentic Bank of America branding** — embedded official logo (flagscape + wordmark), corporate blue palette (`#0066cc`), Bank of America navy/red accents on the debit card preview
- **Premium fintech aesthetic** — deep charcoal surfaces, Inter + JetBrains Mono typography, cohesive design tokens, smooth Vue transitions
- **Hero balance card** with quick-action buttons (Deposit · Withdraw · Transfer · Manage)
- **Grouped transaction history** — Today / Yesterday / weekday / date grouping, type icons, color-coded amounts, search filter, empty states
- **Quick-amount chips** ($50 / $100 / $500 / $1,000 / $5,000 / All cash) on every value-moving form
- **Confirmation modal** with itemized summary for every transaction (deposit, withdraw, internal/external transfer, account delete)
- **Toast notification stack** (top-right slide-in) replacing the cramped legacy banner
- **Polished PIN prompt** — 4-dot indicator, auto-submit on 4th digit, error shake animation, full keyboard support (digits + backspace)
- **Realistic debit card preview** reflecting holder name and last-4 of citizen ID
- **Account number masking** with eye-toggle reveal
- **Live clock** in the topbar, fully-localised time and date formatters
- **Transparent backdrops** — PIN prompt and ATM overlay float over the game world like the legacy bank ledger

## Compatibility

- Built and tested against **QBCore Framework**
- 1:1 NUI contract preserved — all 11 callbacks (`closeApp`, `withdraw`, `deposit`, `internalTransfer`, `externalTransfer`, `orderCard`, `openAccount`, `renameAccount`, `deleteAccount`, `addUser`, `removeUser`) wired identically to upstream qb-banking
- Window-message handlers `openBank` and `openATM` preserved
- All backend data shapes (`playerData`, account rows, statement rows) untouched

## What changed vs. upstream qb-banking

| File | Status |
|------|--------|
| `html/index.html` | **Rewritten** — Vue 3 SFC-style template, inline SVG sprite, BoA branding |
| `html/style.css` | **Rewritten** — design token system, embedded BoA logo PNGs, ~1500 lines |
| `html/script.js` | **Rewritten** — Vue 3 `createApp`, toast stack, confirmation modal, formatters |
| `client.lua` | **Unchanged** |
| `server.lua` | **Unchanged** |
| `config.lua` | **Unchanged** |
| `fxmanifest.lua` | **Unchanged** |
| `banking.sql` | **Unchanged** |
| `locales/*.lua` | **Unchanged** |

## Installation

1. Stop your server.
2. **Back up your existing `qb-banking` resource.**
3. Replace the resource folder with this one (or rename this folder to `qb-banking` if you keep both side-by-side).
4. Make sure the SQL schema from `banking.sql` is already applied (no changes from upstream).
5. Start your server. `ensure qb-banking` runs as normal.

No config edits needed. No client-side changes. No database migrations.

## Recommended pairing

For a fully-themed Bank of America experience pair this resource with:

- **[MrHunter · Bank of America MLO](https://mrhunter.tebex.io/package/5063501)** by **MrHunter** — Bank of America branded interior + ATM exteriors that match this UI's branding.

Together you get:
- Branded exterior signage and ATM kiosks (MLO)
- Branded NUI banking interface (this resource)
- Consistent palette, logo, and tone across every player touchpoint

## Credits

- **Original qb-banking** — [QBCore Framework](https://github.com/qbcore-framework/qb-banking) (GPL-3.0)
- **UI/UX redesign** — this fork
- **Bank of America brand assets** — © Bank of America Corporation, used here for non-commercial fan/mod purposes only
- **Recommended MLO** — [MrHunter](https://mrhunter.tebex.io/package/5063501)

## License

Released under **GPL-3.0**, inheriting from upstream qb-banking. See [LICENSE](LICENSE).

```
QBCore Framework
Copyright (C) 2026 shotbyuno

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.
```

## Disclaimer

This is an unofficial fan modification for the FiveM/QBCore community. **Not affiliated with, endorsed by, or sponsored by Bank of America Corporation.** All Bank of America trademarks, logos, and brand elements are the property of Bank of America Corporation and are used here in good faith for non-commercial fan/modding purposes. If you are a Bank of America representative and would like this resource to use generic branding instead, please open an issue.
