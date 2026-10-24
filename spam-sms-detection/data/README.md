# Data

The dataset is not committed to this repository. To run the notebook, download the **SMS Spam Collection Dataset** from [Kaggle](https://www.kaggle.com/search?q=sms+spam+collection+dataset) (originally from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/)) and place the file here:

```
data/
└── spam.csv
```

The file is Latin-1 encoded; the notebook reads it with `encoding="latin-1"` and keeps the `v1` (label) and `v2` (message) columns.
