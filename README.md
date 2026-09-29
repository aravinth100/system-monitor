# Smart System Health Monitor

An ML-powered system monitoring application that collects system metrics, analyzes resource usage, detects anomalies, and exposes predictions through a FastAPI REST API.

## Features

- CPU monitoring
- Memory monitoring
- Disk monitoring
- CSV-based metric logging
- Pandas-based data analysis
- Matplotlib visualization
- Isolation Forest anomaly detection
- Saved ML model using Joblib
- FastAPI REST API
- Interactive Swagger API documentation

## Machine Learning

The project uses the Isolation Forest algorithm for unsupervised anomaly detection.

The model currently uses:

- CPU usage
- Memory usage

Disk usage is collected and displayed but is not currently used by the ML model because the collected dataset has very little disk-usage variation.

## Project Structure

```text
system-monitor/
│
├── app/
│   ├── __init__.py
│   ├── api.py
│   └── predict.py
│
├── scripts/
│   ├── main.py
│   ├── analyze.py
│   ├── visualize.py
│   ├── anomaly_detector.py
│   ├── train_model.py
│   └── evaluate_model.py
│
├── data/
│   ├── system_metrics.csv
│   └── evaluated_results.csv
│
├── models/
│   └── system_anomaly_model.pkl
│
├── requirements.txt
└── README.md