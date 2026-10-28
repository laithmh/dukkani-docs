# 💼 Portfolio & Resume Showcase Snippets
## Copy, JSON/MDX Frontmatter, Bullet Points & STAR Interview Stories

Use the snippets below to feature **Dukkani (دكّاني)** on your personal website, GitHub portfolio, LinkedIn, and resume.

---

## 🌐 Portfolio Website Copy

### Short Card Summary (150 Characters)
> **Dukkani (دكّاني):** Offline-first Syrian retail POS and USD-pegged debt ledger engineered with Flutter, BLoC, and Drift SQLite for hyper-volatile economies.

### Medium Overview (1 Paragraph)
> **Dukkani (دكّاني)** is a 100% offline-first commercial Point of Sale and inflation-hedged customer debt ledger designed for neighborhood grocery stores in Syria. Engineered with Flutter, strict BLoC architecture, and Drift SQLite, it features zero-floating-point `Decimal` multi-currency math, smart banknote denomination rounding, an append-only double-entry ledger with native SQLite immutability triggers, Ed25519 offline asymmetric licensing, and an elderly-friendly "Salt & Pepper" monochrome design system with strict 56px/64px touch targets.

---

## 🏷️ Structured JSON / MDX Frontmatter

Ready to drop into Next.js, Gatsby, Hugo, or Astro portfolio collections:

```json
{
  "title": "Dukkani (دكّاني) — Offline-First Syrian POS & USD-Pegged Debt Ledger",
  "slug": "dukkani-offline-pos-ledger",
  "role": "Principal Mobile Architect & Full-Stack Flutter Engineer",
  "category": "Mobile & FinTech Architecture",
  "featured": true,
  "stack": [
    "Flutter",
    "Dart",
    "flutter_bloc",
    "Drift (SQLite)",
    "Decimal Math",
    "Ed25519 Cryptography",
    "AES-256-GCM",
    "Clean Architecture"
  ],
  "metrics": {
    "testSuites": 44,
    "floatingPointViolations": 0,
    "touchTargetFloorPx": 56,
    "cloudDependencies": 0,
    "supportedDenominations": "10/25/50 SYP Banknote Grid"
  },
  "summary": "Specialized offline retail POS replacing fragile paper debt notebooks with an inflation-protected append-only financial ledger for Syrian neighborhood merchants.",
  "githubUrl": "https://github.com/laithmh/dukkani-docs",
  "liveDemoUrl": null
}
```

---

## 📄 Quantified Resume Bullet Points

- **Architected a 100% offline-first Point of Sale & Customer Debt Ledger in Flutter & Drift SQLite**, replacing fragile paper debt notebooks with an append-only accounting system for neighborhood grocery stores in volatile currency markets.
- **Engineered an arbitrary-precision multi-currency engine using `Decimal` & custom SQLite type converters**, eliminating 100% of floating-point rounding errors and implementing a cyclic 50-step algorithm that snaps cash checkout totals to physical banknote denominations.
- **Enforced financial data integrity with 4 native SQLite database triggers**, preventing unauthorized updates or deletions on issued invoices and ledger records while maintaining immutable audit trails with double-entry compensating reversals.
- **Designed and developed an asymmetric offline licensing system using Ed25519 digital signatures and hardware device fingerprinting**, enabling commercial activation with zero cloud server dependencies and anti-clock-rollback tamper detection.
- **Created the "Salt & Pepper" elderly-friendly design system**, establishing a WCAG AAA compliant monochrome interface with a mandatory 56px/64px touch target floor and RTL Arabic layout with Western numeral input normalization.
- **Authored 44 automated test suites across 4 layers**, verifying financial rounding boundaries, in-memory SQLite transactions (`NativeDatabase.memory()`), BLoC state transitions, and responsive scaling from 320px devices to tablets.

---

## 🎙️ STAR Interview Stories (Deep Technical Talking Points)

### Story 1: Precision Financial Engineering in a Volatile Economy
- **Situation:** In the Syrian market, wholesale costs are pegged to USD, but daily retail cash checkout occurs in Syrian Pounds, a currency without fractional coins and subject to rapid inflation. Standard software using binary floats (`double`) or basic rounding creates ledger imbalances and unpayable change amounts.
- **Task:** Build a mathematical engine guaranteeing zero floating-point drift, live exchange rate re-pricing, and cash rounding strictly matching physical banknote denominations.
- **Action:** Created `SyrianCurrencyEngine` using arbitrary-precision `Decimal`. Stored all amounts as SQLite `TEXT` via custom Drift converters. Designed a 50-step cyclic denomination grid algorithm that decomposes cash totals and snaps remainders to valid combinations of 10 and 25 SYP notes while preserving exact precision on individual line items.
- **Result:** Complete elimination of rounding discrepancies between store cash drawers and customer ledger records across tens of thousands of simulated checkout transactions.

### Story 2: Database-Level Immutability & Double-Entry Accounting
- **Situation:** Traditional POS apps maintain a mutable `balance` column on customer records, which frequently desynchronizes from transaction history when apps crash, battery dies, or unexpected errors occur.
- **Task:** Architect a reliable ledger where customer debts and payments can never fall out of sync with invoices.
- **Action:** Designed an append-only architecture where customer balances are calculated on-the-fly using SQL aggregations (`SUM(charges) - SUM(payments)`). Enforced immutability by writing native SQLite triggers (`trg_ledger_no_delete`, `trg_ledger_no_update`) directly in the database engine, requiring all corrections to occur through explicit double-entry reversals (`charge_reversal`, `payment_reversal`).
- **Result:** 100% auditability and zero balance corruption. Reversing an invoice automatically marks it void and restores inventory stock inside a single atomic Drift transaction.

### Story 3: 100% Offline Cryptographic Licensing without Cloud Servers
- **Situation:** Recurring power outages and intermittent internet in Syria make cloud-based licensing servers unviable. However, the software required commercial licensing tied to specific merchant hardware to prevent unauthorized copying.
- **Task:** Create an offline licensing and device-binding mechanism that cannot be circumvented by changing the device system clock.
- **Action:** Implemented asymmetric digital signatures using Ed25519 (`cryptography` package). The app embeds only the vendor's public key. Activation tokens contain hardware fingerprints and cryptographic timestamps. Added anti-clock-rollback verification that compares system UTC time against the highest recorded timestamp across SQLite invoice and ledger tables.
- **Result:** Complete offline activation security. Rolling back device clocks to bypass license expiration immediately triggers a tamper alert and halts unlicensed execution without requiring a single network byte.

### Story 4: Accessibility & Design Systems for Elderly Non-Technical Users
- **Situation:** Most neighborhood grocery merchants are older adults working in challenging conditions: direct sunlight on low-cost Android phones with low brightness, or dark shops during power rationing. Modern low-contrast UI trends caused high error rates and slow checkout lines.
- **Task:** Design a high-contrast, zero-friction UI that maximizes speed and eliminates missed taps.
- **Action:** Built the "Salt & Pepper" design system: pure white surfaces, `#2B2B2B` charcoal text (14.1:1 contrast ratio), 1.5px solid borders, and zero drop shadows. Enforced a hard minimum touch target of 56px (64px for checkout buttons) using responsive mathematical floors. Integrated a continuous camera barcode scanner with audio/haptic feedback and automatic Eastern-to-Western numeral normalization.
- **Result:** Drastic reduction in cashier checkout friction, enabling older shopkeepers to ring up multi-item customer carts in under 20 seconds.

