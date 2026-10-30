# Music Classification and Wine Clustering

Two exploratory machine-learning case studies in one Jupyter notebook: music-genre prediction with support vector and random forest classifiers, and wine clustering with K-means and PCA.

**What the notebook demonstrates**

- Inspecting class balance, missing values, feature types, and numerical ranges.
- Creating a reproducible stratified training/evaluation split.
- Fitting a quantile transformation on training data and reusing it for evaluation and inference.
- Comparing numerical-feature classification baselines with accuracy, class-wise reports, and confusion matrices.
- Investigating genre errors with distribution plots and misclassified examples.
- Exploring wine groups using standardized features, inertia, three-dimensional plots, and PCA.

**Run locally**

The analysis was checked using Python 3.12 and the versions in `requirements.txt`.

```sh
python -m venv .venv
```

Activate the environment (`.venv\Scripts\Activate.ps1` in PowerShell or `source .venv/bin/activate` on macOS/Linux), then install dependencies and launch JupyterLab:

```sh
python -m pip install -r requirements.txt
jupyter lab
```

Open `music_classification_and_wine_clustering.ipynb` from this project directory. Place the three expected CSV files under `data/` before running all cells. Input schemas and source information are documented in [data/README.md](data/README.md). CSV inputs and generated predictions are ignored by Git.

**Analysis and interpretation**

The music classifiers use numerical track features and exclude identifiers, artist names, and titles. The selected model parameters come from manual exploration, not a recorded cross-validated search. The evaluation split was reused during that exploration, so the reported scores should not be treated as unbiased final test estimates.

The wine analysis fits four clusters in three standardized measurements: alcohol, colour intensity, and hue. PCA provides a two-dimensional view of those fitted clusters. Four clusters are an exploratory choice rather than a verified count of natural wine categories.



**Recorded run**

| Model | Evaluation accuracy |
| --- | ---: |
| Support vector classifier | 0.5934 |
| Random forest | 0.5797 |

These results come from the notebook's single, previously explored split; the model-selection limitation above applies.

**Files**

| Path | Purpose |
| --- | --- |
| `music_classification_and_wine_clustering.ipynb` | Executable analysis, explanations, results, and plots. |
| `requirements.txt` | Analysis dependencies and JupyterLab. |
| `data/README.md` | Input filenames, schemas, and provenance notes. |
| `.gitignore` | Keeps local data, environments, caches, and generated exports out of Git. |

Running the notebook writes `outputs/music_predictions.csv`. Saved notebook results let readers inspect the analyses without the local CSV files. The notebook retains documentation and tutorial references used in developing the analysis.
