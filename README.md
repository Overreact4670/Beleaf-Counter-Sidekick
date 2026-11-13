# Beleaf Counter Sidekick 6.60

Beleaf Counter Sidekick is a browser-based companion for Dutchie counter and floor workflows. It converts locally selected Dutchie exports into a searchable workspace for product discovery, customer consultations, comparisons, and inventory follow-up.

**GitHub Pages:** [Open Beleaf Counter Sidekick](https://overreact4670.github.io/Beleaf-Counter-Sidekick/)

## Main areas

- **Product Search:** Search products by name, brand, strain, flavor, category, SKU/UPC, or plain-language terms. Narrow results by category, price, potency, cannabinoid, terpene, and other available details.
- **Consultation:** Apply customer-request filters, review recommendation evidence, compare products, and use the temporary basket to organize quantities. The basket is session-only and is not saved in the workspace.
- **Highlights:** Review imported promotions, staff picks, and eligible expiry-markdown suggestions. Suggestions are review aids; Sidekick does not change prices or apply discounts in Dutchie.
- **Operations:** Review inventory and import diagnostics, stock and price flags, package status, and expiration dates.

## Importing Dutchie exports

Use **Update from Dutchie** or the first-run file chooser. An Inventory export is required to populate product and stock results. Catalog, Lab results, and Discounts exports add supporting detail. Supported file types are CSV, XLS, and XLSX. The importer recognizes Inventory, Catalog, Lab, and Discounts files; it does not import a separate Batches export.

Review the import preview, source dates, row counts, and warnings before applying the update. Imports are transactional: when a required validation step fails, the current workspace is left unchanged. Package-level inventory and COA details remain separate; the app does not average lab measurements across packages.

For XLS/XLSX imports, Sidekick first checks for a local `xlsx.full.min.js` file beside the HTML, then tries the official SheetJS 0.20.3 CDN. To use Excel offline, save the official SheetJS 0.20.3 browser reader beside the HTML. CSV imports do not require the Excel reader or an internet connection. Excel imports are limited to 25 MB per file.

## Workspace storage and backups

The primary workspace is stored in IndexedDB in the browser profile and site origin where the app is opened. A localStorage compatibility path is used when IndexedDB is unavailable. The workspace is not automatically shared between browsers, computers, profiles, or site addresses.

Use **Backup & restore** to export a JSON backup, move the workspace to another browser, restore a prior backup, or undo the latest successful import or restore. Keep a backup before clearing browser data or changing devices. A tab that detects a newer save from another open Sidekick tab becomes read-only until it is reloaded, avoiding silent overwrites from stale tabs.

Customer View can be entered from the header. It remains active across reloads in the same tab session. Hold the Customer View control for 1.5 seconds to return to staff view.

## Important limitations

- Sidekick processes only the files selected by staff. It does not connect to Dutchie or retrieve live inventory, prices, package status, or discount eligibility.
- Inventory freshness and sellable quantity depend on the imported source. Verify current package availability, restrictions, and selling prices in Dutchie before quoting or checkout.
- A missing or unknown value is not treated as zero or as confirmed eligibility.
- Cannabinoid and terpene measurements depend on source availability and package matching. Inventory and lab-reported values are labeled separately where available.
- Recommendations organize available records; they do not predict medical effects or replace staff judgment.

## GitHub Pages

The repository includes an `index.html` entry point for the current app. To publish the site, configure repository Pages to **Deploy from a branch**, select **main** and **/(root)** under **Settings → Pages**, and save.

## Project

This is a client-side HTML application. Product data processing and the interface run in the browser; no project server is required.
