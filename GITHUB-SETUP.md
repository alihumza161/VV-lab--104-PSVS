# GitHub Setup Instructions for Task 1

1. Create an empty GitHub repository named `VV-Lab-<RollNo>-PSVS`.
2. Download/unzip this project and open the folder in VS Code.
3. Replace `[Your Name]` and `[Your Roll Number]` in `README.md`.
4. In VS Code, open Terminal and run:

```bash
git init
git branch -M main
git add README.md requirements/PSVS-REQ-v1.0.md
git commit -m "PSVS-REQ-v1.0"
git tag baseline-1
git remote add origin https://github.com/<YOUR-USERNAME>/VV-Lab-<RollNo>-PSVS.git
git push -u origin main
git push origin baseline-1
```

5. Add the remaining files to a defect-analysis branch, making three separate commits:

```bash
git switch -c defect-analysis
git add defect-logs/defect-taxonomy.md
git commit -m "docs: define requirements defect taxonomy"
git add defect-logs/defect-log.md defect-logs/peer-review-comparison.md
git commit -m "docs: record requirements defects and peer review template"
git add reports/defect-summary.md reports/defect-summary-chart.png
git commit -m "docs: add defect summary and chart"
git add .github/ISSUE_TEMPLATE/change-request.md abstractions models operations constraints proofs GITHUB-SETUP.md
git commit -m "docs: add change request and project placeholders"
git push -u origin defect-analysis
```

6. Open a pull request on GitHub with base `main` and compare `defect-analysis`, review it, and merge it.
7. Capture screenshots of the commit graph, tag, defect log, chart, and merged pull request.

If you already created a README or requirements file on GitHub, avoid overwriting it blindly. Either clone the existing repository first or reconcile the files before pushing.

## Important
- The baseline tag must point to the commit containing `requirements/PSVS-REQ-v1.0.md`. If your README commit already exists before the requirements commit, the commands above tag the requirements commit correctly because it is the current HEAD after that commit.
- Complete peer-review results using a real classmate's log.
- Recheck defect category totals and chart counts before final submission.
