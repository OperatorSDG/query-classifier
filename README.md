# Query-Classifier

A BERT-based classifier that distinguishes between Gmail and Calendar queries. For calendar queries, it can also extract a time range from the user's input using natural language expressions.

---

## Features

- **Classifies queries** as either `gmail` or `calendar`.
- **Extracts time ranges** from calendar queries using natural language expressions.
- **Interactive widget** for live testing of queries.
- **Automated evaluation** with detailed test case reporting.
- **Confusion matrix** and metrics for model performance.

---

## System Requirements

- **OS:** Ubuntu 22.04 LTS (or compatible Linux)
- **Python:** 3.10+
- **GPU:** NVIDIA GPU recommended (tested on RTX 3060 12GB)
- **RAM:** 16GB+ recommended

### Python Libraries

- torch
- transformers
- pandas
- scikit-learn
- tqdm
- seaborn
- matplotlib
- dateparser
- ipywidgets

Install all dependencies with:

```bash
pip install torch transformers pandas scikit-learn tqdm seaborn matplotlib dateparser ipywidgets
```

---

## Usage

1. **Prepare Data:**  
   Place your labeled queries in `labeled-queries.csv` (see example in the repo).

2. **Run the Notebook:**  
   Open `queryclassifier-final.ipynb` or `upgrade.ipynb` in Jupyter or VS Code.

3. **Train the Model:**  
   The notebook will guide you through data loading, training, and evaluation.

4. **Test the Model:**  
   - Use the interactive widget to test custom queries.
   - Run the automated test cell to evaluate on `test-set.csv`.

---

## File Structure

- `queryclassifier-final.ipynb` — Main notebook for training, evaluation, and testing.
- `upgrade.ipynb` — Alternate notebook with similar functionality.
- `labeled-queries.csv` — Labeled data for training/validation/testing.
- `test-set.csv` — Diverse test cases for evaluation.
- `README.md` — Project documentation.

---

## Example Queries

- **Gmail:**  
  - "Show me my emails"
  - "Find emails from Alice"
  - "Did I get any mail today?"

- **Calendar:**  
  - "What events do I have this week?"
  - "Show calendar for June 2025"
  - "What's on my agenda?"

---

## Notes

- The time extraction utility is rule-based and works for common time expressions (e.g., "this week", "next month", "June 2025").
- Ambiguous or mixed queries (e.g., "Show me my calendar and emails") are challenging and may require more advanced modeling or labeling.
- For best results, use a GPU for training.

---

## Author
OperatorSDG (Sourojeet Dasgupta)