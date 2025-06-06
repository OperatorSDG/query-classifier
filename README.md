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

## System Specs

- **OS:** Arch Linux
- **CPU:** AMD Ryzen 7 7840HS 
- **GPU:** NVIDIA GeForce RTX 4060
- **RAM:** 32GB

- **Python:** 3.10.X
- **CUDA:** 12.9
- **PyTorch:** 2.5.1, (GPU-CUDA) 11.8

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

**Note:**  
> The interactive widget for live query testing requires the `ipywidgets` library and a Jupyter Notebook environment (such as JupyterLab, Jupyter Notebook, or VS Code with the Jupyter extension).  
>  
> If you run the notebook in a plain terminal or an environment that does not support widgets, the interactive features will not work.  
>  
> **To enable widgets:**  
> ```bash
> pip install ipywidgets
> #JupyterLab
> jupyter labextension install @jupyter-widgets/jupyterlab-manager
> #VScode
> code --install-extension ms-python.python
> code --install-extension ms-toolsai.jupyter
> code --install-extension ms-python.vscode-pylance
> code --install-extension ms-toolsai.jupyter-keymap
> code --install-extension ms-toolsai.jupyter-renderers
> ```
> For classic Jupyter Notebook, just installing `ipywidgets` is usually sufficient.

---
    
## References
- [HuggingFace Transformers Documentation](https://huggingface.co/docs/transformers/index)
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [dateparser Documentation](https://dateparser.readthedocs.io/en/latest/)
- [scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Jupyter Notebook Documentation](https://jupyter-notebook.readthedocs.io/en/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [seaborn Documentation](https://seaborn.pydata.org/)
- [ipywidgets Documentation](https://ipywidgets.readthedocs.io/en/stable/)

---

## Author
OperatorSDG (Sourojeet Dasgupta)