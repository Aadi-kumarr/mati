# Industrial AI for Predictive Maintenance and Operational Intelligence

## Overview

This project presents an end-to-end Industrial AI platform for predictive maintenance, anomaly detection, explainable AI, and agentic maintenance orchestration.

Using the NASA CMAPSS FD004 dataset, the system predicts Remaining Useful Life (RUL), detects abnormal equipment behavior, explains failure drivers, and demonstrates how these capabilities can be deployed within a scalable Azure-native architecture.

The project was developed as part of an Industrial AI Systems assessment focused on real-time manufacturing intelligence, predictive maintenance, and operational AI.

---

## Key Capabilities

### Predictive Maintenance

* Remaining Useful Life (RUL) prediction
* Operating-condition-aware feature engineering
* XGBoost and LightGBM benchmarking

### Anomaly Detection

* Isolation Forest anomaly detection
* Autoencoder anomaly detection
* Early failure identification

### Explainable AI

* SHAP-based explainability
* Root cause analysis
* Failure driver identification

### Agentic AI

* Multi-agent maintenance workflows
* Human-in-the-loop approval system
* Automated maintenance recommendations

### Production Architecture

* Azure-native deployment design
* Real-time telemetry processing
* Continuous monitoring and retraining

---

## Dataset

### NASA CMAPSS FD004

Characteristics:

* 249 engines
* 61,249 telemetry records
* 21 sensor measurements
* Multiple operating conditions
* Multiple fault modes

The dataset was selected because it closely resembles real-world predictive maintenance challenges where equipment operates under varying conditions.

---

## Project Structure

```text
mati-labs-industrial-ai/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_advanced_eda.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_xgboost_baseline.ipynb
│   ├── 05_advanced_features.ipynb
│   ├── 06_xgboost_final.ipynb
│   ├── 07_lightgbm_benchmark.ipynb
│   ├── 08_isolation_forest_anomaly_detection.ipynb
│   ├── 09_autoencoder_anomaly_detection.ipynb
│   └── 10_shap_explainability.ipynb
│
├── architecture/
│   ├── agentic_industrial_ai_architecture.md
│   ├── azure_production_architecture.md
│   └── architecture_diagram.png
│
├── reports/
│   └── executive_summary.md
│
├── models/
│
├── dashboard/
│
├── README.md
└── requirements.txt
```

---

## Model Performance

### Remaining Useful Life Prediction

| Model    |  MAE |  RMSE |    R² |
| -------- | ---: | ----: | ----: |
| XGBoost  | 12.7 |  19.4 | 0.775 |
| LightGBM | 12.7 | 19.35 | 0.776 |

XGBoost was selected as the primary predictive maintenance model.

---

## Anomaly Detection Results

### Isolation Forest

| Metric                  | Value |
| ----------------------- | ----: |
| Mean RUL of Anomalies   |  15.1 |
| Median RUL of Anomalies |     7 |

### Autoencoder

| Metric                  | Value |
| ----------------------- | ----: |
| Mean RUL of Anomalies   |  98.6 |
| Median RUL of Anomalies |    72 |

Isolation Forest demonstrated significantly stronger alignment with impending failure and was selected as the preferred anomaly detection approach.

---

## Explainability Results

SHAP analysis identified the most important degradation indicators:

1. sensor_11_norm
2. sensor_14_norm
3. sensor_9_norm
4. sensor_4_norm
5. sensor_6_norm

These sensors form a degradation signature used for maintenance prioritization and root cause analysis.

---

## Agentic AI Workflow

```text
Telemetry Stream
        ↓
Monitoring Agent
        ↓
Anomaly Detection Agent
        ↓
RUL Prediction Agent
        ↓
Root Cause Analysis Agent
        ↓
Maintenance Planning Agent
        ↓
Human Approval Agent
        ↓
CMMS / ERP System
```

---

## Azure Production Stack

* Azure IoT Hub
* Azure Event Hub
* Azure Databricks
* Delta Lake
* Azure Machine Learning
* Azure OpenAI
* Azure Cosmos DB

The architecture supports real-time inference, drift monitoring, retraining pipelines, and enterprise-scale deployment.

---

## Key Business Outcomes

* Reduced unplanned downtime
* Improved maintenance scheduling
* Explainable maintenance recommendations
* Early anomaly detection
* Real-time operational intelligence
* Scalable Industrial AI deployment

---

## Future Enhancements

* Online learning pipelines
* Reinforcement learning-based maintenance policies
* Multi-asset fleet optimization
* Edge deployment on industrial gateways
* Retrieval-Augmented Generation (RAG) for maintenance knowledge systems

---