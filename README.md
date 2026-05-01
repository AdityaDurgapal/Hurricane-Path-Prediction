# Hurricane IDALIA Path Prediction

A data mining project that predicts the track of Hurricane Idalia (2023)
using machine learning models trained on GIS data from the
National Hurricane Center (NHC).

## Overview

Three models — **Random Forest (RF)**, **RNN**, and **LSTM** — are
benchmarked across four NHC GIS layers: forecast path lines, uncertainty
cone polygons, meteorological forecast points, and watch/warning lines.
Models are evaluated on in-sample GIS training data and on a
**rolling 1-step-ahead forecast** of Idalia using historical HURDAT2 data.

## Results

Random Forest consistently outperforms RNN and LSTM, especially on
geometric layers with limited data. The richest layer (`_5day_pts`)
achieves an MAE of ~0.45° (~50 km) with RF.

## Stack

- **Data:** NHC GIS shapefiles, HURDAT2 historical hurricane database
- **Libraries:** GeoPandas, Scikit-learn, TensorFlow/Keras, Matplotlib, Fiona

## Authors

Abhiraj Akhouri · Subhadip Baidya · Aditya Dinesh Durgapal · Rohak Debnath  
*DMS672: Data Mining & Knowledge Discovery, IIT Kanpur — Summer 2025*
