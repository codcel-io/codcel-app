# Codcel Desktop — Release Notes

A running log of what's new in each Codcel Desktop release.
For binary downloads, see the [README](./README.md) or visit the [releases page](https://github.com/codcel-io/codcel-app/releases).

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
