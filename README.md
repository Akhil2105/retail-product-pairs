# Counting baskets or counting buyers?

**PhDAI-733 · Deliverable 2 · Akhil Kamatam and Snehith Reddy**

Does the number of independent buyers who bought two products on the same invoice improve top-three companion recommendations beyond the number of invoices containing the pair?

## Run the study

1. Open [Google Colab](https://colab.research.google.com/). Choose **File → Upload notebook** and select `Retail_Product_Pair_Study.ipynb`. The source is [UCI Online Retail](https://doi.org/10.24432/C5BW33) (Chen, 2015; CC BY 4.0).
2. Use a CPU runtime and **Runtime → Run all**. Internet is needed on the first run. The notebook downloads and verifies the original UCI archive; reading the workbook can take a few minutes.
3. Check the cleaning audit, the history/fit/test dates and the final metrics. The benchmark counts a missing recommendation as a miss; compare the two logistic rows for the effect of adding distinct-buyer support. The displayed results are from a full-data execution, not a synthetic demonstration.
4. The report is `Retail_Product_Pair_Report.docx`. It contains the four assigned sections. Check it against the rerun, then update the collaboration section with *actual* GitHub/Colab review details.

For a local rerun, use Python 3.12, a fresh virtual environment, and `python -m pip install -r requirements.txt`, then open the notebook in JupyterLab. Colab users do not need this installation step.

## Suggested team review

- **Confirmed:** Akhil Kamatam and Snehith Reddy jointly discussed real-world situations they had encountered and framed the research problem.
- **Next:** Put this folder in the team's GitHub repository and share an editable Colab notebook with the two teammates. No online repository or share link is created by this package.
- Have one teammate reproduce the cleaning audit and the same-invoice unit check in Section 3. Have the other verify the date cutoffs, review the uncovered-anchor rule and rerun the held-out comparison. These are proposed checks, not claimed assignments.
- Use an issue or pull request to record the actual reviewer, date, notebook version/commit, one verified result, and any change. Update the report before submission. Keep the Excel file, cached download, and customer-level exports out of Git; the checked-in notebook has only aggregate and product-level displays.

### Files

- `Retail_Product_Pair_Study.ipynb` — notebook with executed outputs, figures, and a reproducible public loader.
- `Retail_Product_Pair_Report.docx` — written analysis and team process.
- `requirements.txt` — dependencies for an optional local run.
- `.github/pull_request_template.md` — a short review checklist; fill it in only when a review happens.

**Interpretation:** The study predicts companions in recorded multi-item baskets. It does not measure which product was clicked first, customer response to a recommendation, or incremental sales. Do not identify wholesalers from account IDs. AI assistance with the code and written draft is disclosed in the notebook and report.
