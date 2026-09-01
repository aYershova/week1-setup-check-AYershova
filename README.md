# STAT163 Week 1 — setup check

Verifies that Python, `uv` and pandas are installed and working before your first
practice session. **Not graded.** An automatic check marks your commits with a green ✓
or a red ✗.

## Steps

1. Click the green **Use this template** button → **Create a new repository**.
   Owner: your own GitHub account. Name: `week1-setup-check-<your-username>`.
   Visibility: **Public** is fine for this one (there is nothing personal in it beyond
   your name) — but Private also works.
2. Clone your new repository:
    ```
    git clone <your-repository-url>
    cd <repository-folder>
    ```
3. Install [`uv`](https://docs.astral.sh/uv/) if you do not have it:
    - macOS / Linux: `curl -LsSf https://astral.sh/uv/install.sh | sh`
    - Windows (PowerShell): `powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"`
4. Install the dependencies:
    ```
    uv sync
    ```
    `uv.lock` is already in the repository — it pins exact versions, so `uv sync`
    installs precisely those. Do not delete or edit it.
5. Open `check.ipynb`:
    - Jupyter Lab: `uv run jupyter lab`, then click `check.ipynb` in the file browser.
    - Positron: open the repository folder (File → Open Folder), then click `check.ipynb`.
6. In the first code cell, replace `_your name_` with your name.
7. Run every cell in order (`Shift+Enter`). Each must finish without errors.
8. Save the notebook, then commit and push:
    ```
    git add check.ipynb
    git commit -m "Setup check"
    git push
    ```
9. Refresh your repository page on GitHub. Within about a minute a green ✓ appears next
   to your commit if the automatic check passed. A red ✗ means something failed — click
   it to see the details, and bring the error message to your practice session.

## What this check tests

- Python ≥ 3.10 and pandas ≥ 2.0 are installed and importable
- pandas can create and display a `DataFrame`
- The notebook records your OS, CPU architecture and Python version — saved in the
  repository as proof of completion and as diagnostic context that speeds up
  debugging
- Jupyter can execute the notebook top to bottom (the automatic check re-runs it and
  fails if any cell raises)
- **Every code cell was executed and saved.** The check requires saved output in each
  cell — that proves you ran the notebook on your own machine. A notebook committed
  without running (empty outputs) or with a saved error fails. Run every cell
  (`Shift+Enter`) **and save** before `commit`.
