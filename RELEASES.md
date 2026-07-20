# Codcel Desktop — Release Notes

A running log of what's new in each Codcel Desktop release.
For binary downloads, see the [README](./README.md) or visit the [releases page](https://github.com/codcel-io/codcel-app/releases).

---

## release-0.1.8
_The "work with whole tables" release._

Codcel Desktop 0.1.8 moves past single-cell inputs and outputs. You can now feed whole cell **ranges** into a transpiled model, spill **2-D array results** the way Excel's dynamic arrays do, and use Excel's full family of **database functions** — all with sharper error handling and cleaner generated code across every target language.

### New Features
- **Range inputs** — Define inputs as ranges (e.g. `A5:B25`), not just single cells, so one transpiled function can take an entire table of inputs at once.
- **Dynamic arrays & spill ranges** — Formulas that produce a range of results now transpile and evaluate correctly, tracking how values spill across a 2-D region just like Excel.
- **Database functions** — Excel's D-function family (`DGET`, `DSUM`, `DCOUNT`, `DAVERAGE`, `DMAX`, `DMIN` and the rest) is now transpiled and supported in the calculation engine, letting a formula query a labelled table by criteria.

### Improvements
- **New information functions** — `ERROR.TYPE` and `ISNA` let you identify specific errors and tell failed lookups apart from other formula errors.
- **Sharper error handling** — `IFERROR` over a 2-D range now expands per-cell fallback correctly, and errors from database functions are picked up by `ISERROR`, `ISERR` and `ERROR.TYPE`.
- **Cleaner generated code** — Language-specific fixes across Java, C#, Visual Basic, WASM and the Dioxus desktop templates, plus correct string arrays in every target language.

[Download release-0.1.8 →](https://github.com/codcel-io/codcel-app/releases/tag/release-0.1.8)

---

## release-0.1.7

_The "bring your data in" release._

Codcel Desktop 0.1.7 makes it dramatically easier to work with the data that lives **outside** your spreadsheets. You can now open Parquet and CSV files directly inside the app, upload Parquet datasets into your projects, and generate Python interfaces for both desktop and web clients — all without leaving Codcel.

### New Features

- **View Parquet File** — Open any `.parquet` file straight inside Codcel Desktop and browse its contents. No more bouncing between tools just to peek at your columnar data — preview schemas, scan rows, and confirm your inputs are exactly what you expect before you transpile.
- **View CSV File** — Inspect CSV files in-app with the same smooth workflow. Great for sanity-checking inputs, spotting bad rows, and making sure your spreadsheet logic is being fed the right data.
- **Parquet upload & read** — Upload Parquet files into your project and have Codcel read them as first-class data sources. Your generated code can now be backed by real Parquet datasets, so the same Excel logic that powered a prototype can scale up to production-sized data without rewriting a thing.

### New Generators

- **Codcel Excel Python Interface** — Generates an Excel workbook that keeps Excel as the **frontend** while delegating every calculation to a Codcel-generated Python library under the hood. Cells call into Python through VBA and xlwings, so your users keep the spreadsheet they already know and love — but the formulas they're hitting are now real, tested, version-controlled Python code instead of fragile sheet logic.
- **Codcel Excel Web Client Python Interface** — Same idea, but the Excel frontend talks to a Codcel-generated web service instead of a local library. VBA and xlwings wire Excel up to a Python web client that calls your Codcel API, so a single workbook on a user's laptop can be powered by a centrally-deployed service. Update the math once on the server and every Excel user gets it instantly — no redistributing spreadsheets, no version drift.

### Improvements

- Various minor bug fixes and stability improvements.

[Download release-0.1.7 →](https://github.com/codcel-io/codcel-app/releases/tag/release-0.1.7)

---

## release-0.1.5

The initial public release of Codcel Desktop.

[Download release-0.1.5 →](https://github.com/codcel-io/codcel-app/releases/tag/release-0.1.5)
