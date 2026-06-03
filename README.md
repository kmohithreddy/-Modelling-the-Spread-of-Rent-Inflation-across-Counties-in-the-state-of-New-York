
# Modelling the Spread of Rent Inflation across Counties in the state of New York through a Combined Spatial Analysis and Diffusion Modeling Approach

## Overview

The spread of rent inflation across the US has reduced the affordability of housing, especially for young people
in the country. Despite injection of investment being a factor for rent inflation, it is important for economic growth.
The federal and state governments therefore face a dilemma of continued economic growth at the expense of
house affordability. Hence, there is a need to observe rent inflation from the perspective of how it diffuses from
target areas of investment injection, as a management approach rather than discouraging injection of investment all
together. This project employed spatial analysis and diffusion modeling in order to provide an understanding of
how rent inflation spreads overtime and across counties in the state of New York.

## Data

Data for the project was collected from:

• Census.gov for historical housing units data

• Bureau of Economic Analysis for historical investment data (GDP PI) and historical personal income data per county

• FRED for historical national investment dats 

• HUDUSER for rent data per county

## Packages

``` Python
# Core
!pip install numpy pandas matplotlib seaborn scikit-learn

# Deep Learning
!pip install torch torchvision torchaudio

# Gradient Boosting
!pip install xgboost

# Geospatial (for adjacency / shapefiles)
!pip install geopandas shapely fiona pyproj rtree libpysal

# Utilities
!pip install tqdm
```

``` Python
# Core
import numpy as np
import pandas as pd

# Visualization
import matplotlib.pyplot as plt
import seaborn as sns

# Machine Learning
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score

# XGBoost
from xgboost import XGBRegressor

# Deep Learning (PyTorch)
import torch
import torch.nn as nn
import torch.optim as optim
from torch.utils.data import DataLoader, TensorDataset

# Geospatial
import geopandas as gpd
import libpysal

# File Handling
import zipfile
import os
import io
import requests

# Utilities
from tqdm import tqdm
```






## Diffusion Model - ConvLSTM

<img width="1725" height="286" alt="Figure 1" src="https://github.com/user-attachments/assets/b4764bf5-5d03-4b80-8ece-3f9ea625379a" />


## Time Series Models - XGBoost and LSTM 

<img width="982" height="542" alt="Figure 2" src="https://github.com/user-attachments/assets/178cf449-23d0-49da-a423-8a284b4e1821" />


## Spatial Analysis

<img width="1016" height="595" alt="image" src="https://github.com/user-attachments/assets/c342b616-5078-4891-a3cb-4cd4a8ce67c0" />


### Hotspot Analysis

<img width="893" height="595" alt="image" src="https://github.com/user-attachments/assets/569f2f2d-4330-448f-abf7-a1140d3f47e9" />


## Rent Inflation Diffusion 

<img width="1830" height="929" alt="image" src="https://github.com/user-attachments/assets/969dce28-45d2-4e33-bddc-1ca645292366" />


## Model Performance Comparison

<img width="845" height="417" alt="Table 3" src="https://github.com/user-attachments/assets/996e7566-a6ef-4d44-8a5f-7de30663fd2c" />












