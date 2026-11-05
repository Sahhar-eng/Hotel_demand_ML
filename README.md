# Hotel_demand_ML
 
a machine learning project for a hotel booking booking system 
github url : https://github.com/Sahhar-eng/Hotel_demand_ML.git
## Classification workflow

1. `src/Notebooks/general_EDA.ipynb`: inspect and clean source data.
2. `src/Notebooks/classification_feature.ipynb`: training-only cancellation EDA, eligible input selection, chronological splitting, and CSV export.
3. `src/Notebooks/classification_model.ipynb`: load CSVs and fit imputation, standard scaling, one-hot encoding, and logistic regression in one pipeline. The notebook is supplied unexecuted; running its training cell fits the model. Test evaluation is disabled by default.

Current data lives in `src/data/classification_features/basic/`: `train.csv`, `validation.csv`, `test.csv`, and `split_summary.csv`. EDA figures are in `plots/`. The split CSVs contain unscaled, unencoded inputs, the `IsCanceled` target, and a `source_row_id` that must not be used as a predictor. No JSON, NPZ, or joblib files are needed for this workflow.

The source EDA's target-dependent zero-guest filtering and deduplication assumptions still need review. The historical test cohort was inspected in an earlier experiment; use a fresh future holdout for an unbiased final evaluation of later choices.
