# Beleaf Counter Sidekick

Beleaf Counter Sidekick is a browser-based helper for cannabis retail counter and floor workflows. It turns Dutchie export files into a searchable product workspace for product discovery, side-by-side comparisons, inventory checks, and shift follow-up.

## What it does

- **Find products quickly:** Search product names, brands, flavors, categories, and preferences. Narrow results by category, budget, potency, terpenes, and other available details.
- **Support customer conversations:** Use consultation filters and saved staff picks to explore options. Compare up to three products, and switch to Customer view to hide staff-only details such as stock, vendor, and SKU.
- **Review product information:** See package-specific details when available, including price, quantity, expiration, listed potency, cannabinoids, and lab-reported terpene profiles.
- **Keep floor work visible:** Review products nearing expiration, low stock, price differences, discounts, and import matching details. Use shift tasks to track follow-ups.
- **Refresh from exports:** Import Dutchie Inventory, Catalog, Lab, and Discounts data from CSV or Excel files. Review the import summary and warnings before applying an update.
- **Back up the workspace:** Export and restore a JSON backup, and undo the most recent import or restore.

## Data and privacy

The app works from files you import. It does not connect to Dutchie or fetch live inventory. Product and inventory data can become outdated, so confirm current availability and selling prices in Dutchie before checkout.

The saved workspace is stored in the browser profile for the site address where the app is opened. It is not automatically shared across browsers or computers. Use **Backup & restore** to move the workspace. The project starts with an empty workspace unless that browser already has a saved import; current inventory is not bundled into the app.

## Getting started

1. Open the Beleaf Counter Sidekick HTML app in a modern browser.
2. Choose **Update from Dutchie** and select the export files you want to import. An Inventory export is needed to populate product and stock results; Catalog, Lab, and Discounts files add supporting details when available.
3. Review the import preview, source dates, row counts, and warnings, then apply the update.
4. Use **Counter mode** for product discovery, **Floor operations** for stock and shift work, and **Backup & restore** to save or move the workspace.

CSV imports work offline. Excel workbook imports load the SheetJS 0.20.3 browser reader from the official SheetJS CDN; if it cannot be reached, export the report as CSV and import that instead. Excel imports are limited to 25 MB per file.

## Notes

- Search and consultation results organize the imported information; they do not establish medical effects or replace staff judgment.
- Terpene and cannabinoid details depend on the source data and package match. Listing values and lab measurements are labeled separately where available.
- Discount eligibility and expiration dates should be checked against the current Dutchie records.

## Project

**Current app version:** 6.27.0

This is a lightweight, client-side HTML app built for Beleaf counter workflows. The app's data processing and interface run in the browser, with no project server required.
