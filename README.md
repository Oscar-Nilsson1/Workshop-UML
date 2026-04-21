# Unsupervised Machine Learning Workshop

A hands-on group workshop on unsupervised learning (clustering), with integrated Git collaboration practice.

## Prerequisites

- Python 3.8+
- Required packages:
  ```bash
  pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
  ```

## Git workflow for students

This workshop integrates Git collaboration. You work in groups of 2-3.

1. **One person forks** this repository on GitHub
2. **Add groupmates as collaborators** (Settings → Collaborators)
3. **Everyone clones** the same fork:
   ```bash
   git clone https://github.com/<FORK-OWNER>/Workshop-UML.git
   cd Workshop-UML
   ```
4. **Parts 0-1:** Work together on `main` — data loading and scaling
5. **Part 2:** Each member creates a branch for one algorithm:
   ```bash
   git checkout -b experiment/kmeans        # member 1
   git checkout -b experiment/agglomerative  # member 2
   git checkout -b experiment/dbscan         # member 3
   ```
6. **Commit and push** your experiment branch:
   ```bash
   git add unsupervised_ml_workshop.ipynb
   git commit -m "Complete experiment: <algorithm>"
   git push -u origin experiment/<algorithm>
   ```
7. **Open Pull Requests** from each branch to `main`
8. **Review** each other's PRs, compare results, and **merge**
9. **Part 4:** Synthesize as a group on `main`

## Workshop structure

| Part | Topic | Time | Who |
|------|-------|------|-----|
| 0 | Repository & Group Setup | ~10 min | Group |
| 1 | Data Preparation & Scaling | ~20 min | Group |
| 2 | Clustering Experiments | ~45 min | Individual (one algorithm per branch) |
| 3 | Pull Requests & Comparison | ~20 min | Group |
| 4 | Synthesis | ~15 min | Group |

Total: ~2 hours

## Difficulty levels

- \* Basic — everyone should complete these
- \*\* Intermediate — aim for these if you are comfortable with scikit-learn
- \*\*\* Challenge — stretch goals for experienced students

## Datasets

You can bring your own dataset (any tabular CSV with numerical columns), or use one of these:

- **Mall Customers** (200 rows) — [Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)
- **Wholesale Customers** (440 rows) — [UCI ML Repository](https://archive.ics.uci.edu/dataset/292/wholesale+customers)
- **Penguins** (344 rows) — built into seaborn: `sns.load_dataset('penguins')`

## Files

```
Workshop-UML/
├── README.md
└── unsupervised_ml_workshop.ipynb   ← student notebook
```

## License

Free to use for teaching purposes.