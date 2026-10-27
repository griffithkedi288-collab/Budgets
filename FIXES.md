# Pocket Budget fixes

Changed files: app/(tabs)/index.tsx, lib/ledger.ts, lib/storage.ts, lib/format.ts

1. Review button now switches to Budgets and scrolls to Monthly bills.
2. Tap anywhere on a budget row to edit: rename, set planned UGX amount, move money in.
3. New "Move money" screen: put money into any budget from Not yet budgeted, savings or another budget.
4. Paying a bill with too little money opens a Pay bill screen: pick another source, or move the shortfall from Not yet budgeted and pay in one tap.
5. Bills can be edited and deleted (tap the bill).
6. Top "Budget" total only counts active budgets (fixes UGX 50,000 vs 0 mismatch); old orphan budgets are cleaned on load.
7. Dates use the phone's local time (todayISO and monthKey were using UTC, so entries made after midnight in Uganda got yesterday's date).
