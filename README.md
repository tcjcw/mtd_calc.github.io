# Making Tax Digital Calculator

A lightweight, browser-based tool to help self-employed individuals and sole traders track income and expenses for HMRC's Making Tax Digital (MTD) for Income Tax scheme. No account or installation required — everything runs in your browser and your data stays on your device.

---

## Features

- **Income tracking** — log income with date, amount, employee pension, employer pension, and notes
- **Expense tracking** — log expenses across HMRC-recognised categories including mileage, travel, professional fees, office costs, rent/bills, and more
- **Mileage calculation** — automatically calculates claimable mileage amounts using the HMRC approved rate
- **Recurring records** — add repeating income or expenses by day, weekday, week, month, or year, with flexible day-of-week and day-of-month controls
- **Quarterly summary** — dashboard view showing income and expenses broken down by tax quarter (Q1–Q4)
- **Tax year enforcement** — records are locked to a single tax year; the app warns you if you attempt to add a record outside the active year
- **Quarter filtering** — filter income and expense tables by quarter or notes
- **Save to Excel** — export all records to a `.xlsx` file organised by quarter, ready for your accountant or MTD submission
- **Load from file** — reimport previously exported `.xlsx` or `.csv` files to continue where you left off
- **Local storage** — records persist in your browser between sessions; no server or account needed
- **Works offline** — once loaded, the app does not require an internet connection
- **iPad friendly** — can be installed to the iPad home screen as a Progressive Web App (PWA)

---

## Getting Started

The app runs entirely in the browser. Simply open `index.html` directly, or visit the hosted GitHub Pages URL:

```
https://tcjcw.github.io/mtd-calc/
```

No installation, sign-up, or server required.

### Adding to iPad Home Screen

1. Open the app URL in **Safari** on your iPad
2. Tap the **Share** button
3. Tap **Add to Home Screen**
4. The app will open full-screen like a native app

---

## Usage

### Dashboard
The dashboard shows a running summary of total income, total expenses, and net profit for the active tax year, along with a quarterly breakdown table.

### Income Tab
Enter the date, amount, and optionally pension contributions and a note (e.g. employer name). Tick **Make recurring** to bulk-add repeating income entries up to an end date.

### Expenses Tab
Select an expense category, enter the date and amount, and set the claimable percentage (defaults to 100%). For mileage, enter miles driven and number of passengers instead — the claimable amount is calculated automatically.

### Saving Your Data
Click **Save to Excel** to download your records as a `.xlsx` file. Each tax quarter is saved as a separate sheet. **Do this regularly** — browser storage can be cleared if you clear your browser data.

### Loading Previous Data
Click **Load progress** and select a previously exported `.xlsx` or `.csv` file to restore your records. Duplicate entries are automatically skipped.

---

## Tax Year Handling

The app enforces a single active tax year (6 April – 5 April) across all records. When you add your first record:
- If the date is in the **current** tax year, it is set as the active year automatically
- If the date is in a **different** tax year, you will be prompted to either switch to that year or cancel

Once records exist, all new entries must fall within the same tax year.

---

## Expense Categories

| Category | Description |
|---|---|
| Other | Miscellaneous allowable expenses |
| Car Travel | Mileage-based claims at HMRC approved rate |
| Non-Car Travel | Trains, buses, taxis, flights |
| Prof. Fees | Accountancy, legal, subscriptions |
| Office | Stationery, phone, equipment |
| Rent/Bills | Business premises, utilities |
| Banking | Bank charges, interest |
| Repairs | Maintenance of business assets |
| Goods Sold | Cost of goods or materials |
| Staffing | Wages, subcontractors |
| Advertising | Marketing and promotion |
| Insurance | Business insurance premiums |

---

## Data & Privacy

All data is stored locally in your browser using `localStorage`. Nothing is sent to any server. Clearing your browser data will erase your records — use **Save to Excel** regularly to back up your data.

---

## Technology

- HTML, CSS, JavaScript — no frameworks or build tools required
- [Bootstrap 5](https://getbootstrap.com/) for layout and UI components
- [Bootstrap Icons](https://icons.getbootstrap.com/) for icons
- [SheetJS (xlsx)](https://sheetjs.com/) for Excel import and export

---

## Disclaimer

This tool is intended to help organise records for MTD submissions and is not a substitute for professional tax advice. Always verify your figures with a qualified accountant before submitting to HMRC.
