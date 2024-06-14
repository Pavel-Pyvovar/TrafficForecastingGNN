# Short-term Traffic Forecasting Using Graph Neural Networks on Taxi Data
This folder contains notebooks created as part of the Industrial Master's Program organised by the University of Tartu and supported by Bolt. The notebooks implement data preprocessing, baselines, graph neural networks (GNNs) and evaluation of the models. The work has been done between June 2023 and 2024 and resulted in a [Master's thesis](https://comserv.cs.ut.ee/ati_thesis/datasheet.php?id=79693).

The following is a brief description of the content of each notebook:
* Traffic data preprocessing
    - downloading map-matched data
    - performing road segment interpolation
    - cutting off the first and last 10% of points
    - filtering a dataset using a bounding box
    - aggregating samples by edge and time interval
    - extracting historical speed features
* Naive baselines
    - defining historical average baselines
    - imputing missing values
    - structuring the dataset as snapshots
    - evaluating baselines
* Linear regression
    - preparing dataset
    - applying linear regression to edges
* LightGBM
    - imputing missing values
    - preparing data for LightGBM
    - training LightGBM
    - saving results to S3
* GNN on a 20-hop subgraph
    - loading preprocessed tracking data
    - extracting a k-hop subgraph
    - preparing the dataset for a GNN
    - training a GNN
    - evaluating baselines
    - visualising speed time series
* GNN architecture comparison
    - preparing data
    - imputing missing values
    - defining variations of a GNN architecture
    - experiments with each GNN architecture with and without target normalisation
    - visualising time series
* DummyGNN
    - implementing the best GNN architecture out of those we tried
    - imputing data
    - preparing the PyTorch dataset
    - training the GNN
* Evaluate short-term traffic forecasting models
    - loading predictions from models
    - plotting edge error histogram
    - computing error metrics (MAE, MSE, MAPE)
    - plotting speed time series
* Count and visualise data imputation methods
    - imputing and counting missing values
    - visualising speed time series for the ground truth and imputed data
* A3TGCN
    - an experiment with the [A3TGCN architecture](https://arxiv.org/abs/2006.11583)
    - imputing missing values
    - training A3TGCN model
    - visualising time series