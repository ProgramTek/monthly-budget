# Monthly Budget

**A Windows budgeting app that helps you plan each month, track paid bills, and see your whole year.**

Monthly Budget is developed by **Programmatic Technologies, LLC**. It is donationware: free to use, with optional donations to support development.

## Download and install

Open **Releases** in this repository and download **MonthlyBudget-Setup-v0.1.14.exe** from the release's **Assets** section. Choose the `.exe` installer; the automatically generated source archives are not the installer.

Version **0.1.14** is a pre-release. Feedback and bug reports are welcome.

1. Run the installer on your Windows PC.
2. Follow the setup prompts. If SQL Server LocalDB is missing, follow the instructions below.
3. Launch **Monthly Budget** using the desktop or Start menu shortcut.

No ZIP extraction, development tools, or separate .NET runtime installation is needed. The installer currently is unsigned, so Windows may display an unknown-publisher or SmartScreen warning.

### System requirements

- Windows 10 or Windows 11 on an Intel/AMD **64-bit (x64)** PC.
- Microsoft SQL Server Express **LocalDB**, version 2016 or later.
- Internet access for downloading the app and any missing prerequisites. Everyday budgeting works offline.

ARM-based Windows PCs are not supported by this installer.

### If LocalDB is missing

The installer checks for LocalDB and guides you through installing it:

1. Select **Download LocalDB** in setup.
2. In Microsoft's downloader, choose **Download Media**, then **LocalDB**.
3. Download and run **SqlLocalDB.msi**. Microsoft setup may request administrator approval.
4. Return to the Monthly Budget installer and select **Check again**.

Installing a regular SQL Server instance alone does not provide the LocalDB component required by this app.

## Features

- **Monthly budgets:** Organize income and expenses into categories, with planned amounts and payment checkboxes.
- **Automatic saving:** Valid changes save automatically as you work.
- **Optional due dates:** Assign due dates to expense items. Dates appear below each item's description, and overdue unpaid items are highlighted.
- **Easy editing:** Click an expense description to open its item editor.
- **Copy a month:** Reuse visible categories, items, and planned amounts for another month. Paid/received checkboxes reset, and due dates shift to the new month.
- **Multiple years:** Switch years to see one year's months at a time. Year navigation begins at 2026.
- **Annual Overview:** View a read-only summary with monthly comparisons, annual category and item totals, payment status, due-date information, and detailed budget rows. Export annual details to CSV.
- **Hide and restore:** Deleted items and categories are hidden and excluded from totals and reports. Use **Show hidden rows** to restore them.
- **Utilities:** Back up all budgets, import compatible files, or permanently delete all budget data.
- **Support tools:** Generate a diagnostic log to attach to a bug report or feature request.

Checking an item as paid or received counts its full planned amount. Partial payments and transaction history are not supported in this version.

## Getting started

1. Select a year and create a month.
2. Add income and expense categories, then add your budget items and planned amounts.
3. Add optional due dates to expenses using the item editor.
4. Check items as income arrives or bills are paid.
5. Open **Annual Overview** to review the selected year's progress.
6. Copy an existing month when you are ready to plan the next one.

Changes save automatically. A backup is a separate file you create manually through **Utilities**.

## Your data and backups

Budget data is stored locally in SQL Server LocalDB for your current Windows account. No cloud account, bank connection, or multi-device synchronization is required or provided. The app does not automatically send your budgets or diagnostic logs anywhere.

Use **Utilities → Back up all budgets** to save a JSON backup containing all years, payment status, due dates, and hidden items and categories. Keep a copy somewhere safe, especially before updating or changing computers. Backup files are not encrypted.

Use **Utilities → Import workbook / backup** to import a Monthly Budget JSON backup or a workbook using the compatible Budget Tools layout. Importing keeps existing months and skips matching months; it does not overwrite them. Arbitrary Excel workbooks and bank statements are not supported. Annual CSV exports are reports, not full backups.

### Updates and uninstalling

Close Monthly Budget, then run the newer installer using the same Windows account. Setup updates the application while retaining your existing budgets. Installing an older version over a newer version is blocked.

Uninstalling Monthly Budget leaves its budget database intact. To erase it deliberately, use **Utilities → Delete All Budget Data**. This permanently deletes visible and hidden budgets and requires typing `delete my data` before the delete button becomes available. Existing exported backup files are kept.

## Bugs and feature requests

Email **support@programmatic-technologies.com**.

Please be specific. For a bug report, include:

- The steps needed to reproduce the problem.
- What you expected and what actually happened.
- Any exact error message and helpful screenshots.
- The diagnostic log from **Report a Bug → Save Log As…**.

The log includes the app version, Windows version, and recent technical events. Budget names and values are excluded. Review screenshots and attachments before sending; nothing is emailed automatically.

For a feature request, describe the behavior you would like and the problem it would solve.

## Support development

Monthly Budget is free to use. If you enjoy the app and would like to support its development, a small donation is appreciated and entirely optional.

| Service | Account |
| --- | --- |
| Cash App | **$MikeAbrown3509** |
| Venmo | **@Michael-Brown-4899** |

Both accounts belong to **Michael Brown**. Open **Donate to the developer** in the app for QR codes, account-copy buttons, and payment links.

---

Copyright © 2026 Programmatic Technologies, LLC.

This repository provides public downloads and application information. Free use of the application does not grant an open-source license to its code.
