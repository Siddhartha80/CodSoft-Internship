# Data

The dataset is not committed to this repository (it is several hundred MB). To run the notebook, download the **Credit Card Transactions Fraud Detection Dataset** (simulated transactions, 2019-2020) from [Kaggle](https://www.kaggle.com/search?q=credit+card+transactions+fraud+detection+dataset) and place the training file here:

```
data/
└── fraudTrain.csv
```

The notebook uses `fraudTrain.csv` only and creates its own stratified 80/20 train/test split.
