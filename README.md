# Census-Data-Workflows
This repo contains two end-to-end notebooks built on the **Census Bureau / Census Income** style dataset


- **`Classification Model.ipynb`** — supervised learning to predict **income group** (`<=50K` vs `>50K`)
- **`Segmentation.ipynb`** — unsupervised learning (K-Means) to create **personas/segments** for marketing-style analysis

Both notebooks are designed to be runnable top-to-bottom in Jupyter.


## 1) What you need (data files)
Here the Data is kept in Data.zip.

Place these files in the **same folder** as the notebooks (repo root recommended):

- `census-bureau.data` — raw data (comma-separated rows)
- `census-bureau.columns` — one column name per line
- (generated) `census-bureau.csv` — created by the classification notebook (or you can create it yourself)

**Important:** `Segmentation.ipynb` expects `census-bureau.csv` to exist.

---

## 2) Environment setup

### Option A: pip (quick)

pip install -U pip
pip install numpy pandas matplotlib scikit-learn joblib xgboost



### Option B: conda

conda create -n census-ml python=3.10 -y
conda activate census-ml
conda install -y numpy pandas matplotlib scikit-learn joblib
conda install -c conda-forge xgboost
