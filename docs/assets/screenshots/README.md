# 📸 Dukkani Screenshot & Demo Assets Guide

This directory houses visual assets for the GitHub repository and portfolio showcase. 

When exporting screenshots or screen recordings from an emulator or physical device, follow the naming guidelines and suggested scenarios below so that the relative markdown image links in `docs/` and `README.md` display properly.

---

## 📐 Recommended Device Specs for Screenshots

- **Mobile Viewports:** `360 x 800` or `390 x 844` logical pixels (Android or iOS).
- **Tablet / POS Terminal Viewports:** `800 x 1280` or `1200 x 1920` (Landscape orientation to showcase the `PosTabletLayout` master-detail view).
- **Format:** High-resolution `.png` or compressed `.webp` with no drop-shadow borders (the app already has crisp 1.5px borders).

---

## 🗂️ Shot List & Pre-Wired Filenames

| Filename | Screen / Modal | What to Showcase in the Frame |
| :--- | :--- | :--- |
| **`01_pos_quick_grid.png`** | POS Home (Mobile) | Pinned live exchange rate top bar (`1 USD = 150 SYP`), 4-digit quick grid items (bread, eggs, milk), and sticky cart bar showing item count and total. |
| **`02_pos_checkout_modes.png`** | Checkout Bottom Sheet | Multi-mode checkout tabs (**نقدي** Cash, **دين كامل** Full Debt, **دفع جزئي** Partial Payment), change calculator, and 64px Dark Pepper execution button. |
| **`03_continuous_scanner.png`** | Scanner Screen | Continuous camera viewfinder with high-contrast target reticle, top HUD, and bottom cash-received console. |
| **`04_weight_calculator.png`** | Weight/Cash Dialog | Weight-by-SYP calculator showing *"بـ 5,000 ل.س زيتون"* converting automatically to grams precision (`0.350 كغ`). |
| **`05_debt_ledger.png`** | Debt Ledger Screen | Customer list showing outstanding USD and SYP balances, search bar, and high-contrast red debt warning badges. |
| **`06_customer_statement_whatsapp.png`** | Customer Detail Screen | Customer ledger timeline showing charges, payments, and the WhatsApp share sheet previewing Arabic formatted debt statements. |
| **`07_inventory_dual_currency.png`** | Product Form Sheet | Synchronized dual USD & SYP price inputs, wholesale carton/box fields, and Quick Code assignment. |
| **`08_analytics_and_cash_drawer.png`** | Analytics Dashboard | Daily cash drawer closing breakdown (expected physical cash in drawer), net USD profit, and debt aging alert card. |
| **`09_tablet_master_detail.png`** | POS Screen (Tablet >= 600dp) | Master-detail split layout: Left 40% persistent cart with checkout button; Right 60% quick grid and category tabs. |

---

## 🎥 Optional Screen Recordings (GIF / MP4)

- **`pos_rapid_checkout.gif`:** 10-second clip demonstrating barcode scan $\rightarrow$ cash checkout $\rightarrow$ success dialog.
- **`held_carts_workflow.gif`:** 8-second clip parking cart #1, ringing up cart #2, and resuming cart #1.
- **`whatsapp_statement_demo.gif`:** 6-second clip tapping the WhatsApp button on a customer profile and opening the pre-filled Arabic message in WhatsApp.

