1. Data ingestion — pull raw data from its source (files, database, API, streaming) into a consistent format.
2. Data validation/cleaning — check for missing values, duplicates, outliers, schema mismatches. Garbage in, garbage out — this stage usually eats the most time.
3. Feature engineering — transform raw fields into model-ready inputs: encoding categoricals, scaling numerics, creating derived features, handling text/images if relevant.
4. Train/validation/test split — carve out data so you can honestly evaluate generalization. Watch for leakage (e.g., time-series data needs chronological splits, not random ones).
5. Model training — pick a baseline model first (simple, fast) before reaching for something complex. Track experiments (hyperparameters, metrics) so results are reproducible.
6. Evaluation — metrics appropriate to the task (accuracy/F1 for classification, RMSE/MAE for regression, etc.), plus error analysis to see where it fails.
7. Deployment — batch scoring, a REST API, or embedded in an app, depending on how predictions get used.
8. Monitoring — track prediction quality and data drift over time, since real-world data shifts.