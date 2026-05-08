# Changelog

All notable changes to this fork of qb-banking are documented here.

## [1.0.0] — Bank of America Edition

### Added
- Complete UI/UX rewrite of `html/index.html`, `html/style.css`, `html/script.js`
- **Authentic Bank of America branding** with embedded official logo (flagscape + wordmark) on the sidebar, ATM header, and PIN prompt
- **Hero balance card** on the Overview tab with quick-action buttons
- **Grouped transaction history** (Today / Yesterday / weekday / date) with type icons and color-coded amounts
- **Transaction search filter**
- **Quick-amount chips** ($50 / $100 / $500 / $1,000 / $5,000 / All cash) on deposit, withdraw, and ATM forms
- **Confirmation modal** with itemized summary for every value-moving action
- **Toast notification stack** (top-right, slide-in)
- **Live clock** in the topbar
- **Account number masking** with eye-toggle reveal
- **Realistic debit card preview** with holder name and last-4 of citizen ID
- **Polished PIN flow** — 4-dot indicator, auto-submit on 4th digit, error shake animation, full keyboard input support
- **Vue transitions** (`<Transition>` and `<TransitionGroup>`) between views, modals, toasts, and transaction list
- Empty state for accounts with no transactions
- Inter (UI) + JetBrains Mono (numbers / IDs) typography from Google Fonts

### Changed
- Color palette shifted from emerald fintech to **Bank of America corporate blue** (`#0066cc`)
- Debit card preview redesigned with Bank of America navy gradient
- All overlays (PIN prompt, ATM card) now have transparent backdrops so the game world remains visible — matching legacy bank ledger behaviour

### Preserved
- All 11 NUI callbacks (`closeApp`, `withdraw`, `deposit`, `internalTransfer`, `externalTransfer`, `orderCard`, `openAccount`, `renameAccount`, `deleteAccount`, `addUser`, `removeUser`)
- Both window-message handlers (`openBank`, `openATM`)
- All backend data shapes, account rows, and statement rows
- `client.lua`, `server.lua`, `config.lua`, `fxmanifest.lua`, `banking.sql`, and all locale files (byte-identical to upstream)
