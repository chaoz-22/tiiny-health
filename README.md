# Tiiny Health

**Review checkup reports privately with your Tiiny Pocket.**

Tiiny Health is a single-file browser app for interpreting lab results, comparing checkups, and preparing questions for a doctor. Open it locally, connect it to your Tiiny, and stream an English Markdown analysis. No installation or build step is required.

## Quick start

1. Open [index.html](./index.html) on GitHub, download the raw file, and open the saved file in a modern browser.
2. In **API settings**, keep the default base URL, `http://openai.api.tiiny/v1`, or enter your Tiiny device’s local address. Copy the API key from TiinyOS and paste it into the app.
3. Click **Connect**. The app discovers available models and selects a chat model automatically. Check the connection status for the model name.
4. Enter a **Report title** and **Checkup date**. Upload a text-based PDF or paste the relevant lab results into **Report text**.
5. Remove personal identifiers, check **I removed personal identifiers**, and click **Analyze Report**.

For Tiiny API setup details, see the [Tiiny developer documentation](https://dev.tiiny.ai/).

## What the analysis includes

| Section | What to look for |
| --- | --- |
| Abnormal biomarkers | Values, units, reference ranges, and abnormal or borderline flags. |
| Clinical correlations | How findings may relate and where more context is needed. |
| Historical trends | Changes between comparable results when a previous checkup summary is included. |
| Visit preparation | Practical next steps and three questions to bring to your doctor. |

Completed analyses are saved locally. Open **History & Backup** to revisit a report by title and date, or use **Copy Markdown** to copy its analysis. Use **Export JSON** and **Import JSON** to move or restore saved records.

## Privacy and storage

- PDF text is extracted in your browser. The app sends the report text and any enabled prior summary to the configured local Tiiny API for analysis.
- Report titles, saved reports, connection settings, and the API key are stored in the current browser’s local storage. They are not automatically synced to GitHub or to another browser.
- JSON backups contain report text and analyses. Keep them somewhere private. The app does not include the API key in those backups.

## Troubleshooting

| If you see… | Try this |
| --- | --- |
| A connection or HTTP 401 error | Verify the local address and API key, and check that your browser can reach Tiiny. |
| No chat model available | Load a text-generation model in TiinyOS, then click **Connect** again. |
| No selectable PDF text | Use a PDF with selectable text, or paste text from a local OCR tool. |
| Slow generation | Test a shorter report with history disabled, or try a smaller chat model in TiinyOS. |

> Tiiny Health is for health management reference. AI-generated summaries do not constitute a clinical diagnosis. Review the original results with a qualified healthcare professional.
