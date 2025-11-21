# Nigerian Telecom Edge Computing Load Data Project

# Introduction

Picture a farmer in rural Ogun State using sensors to monitor soil moisture or a traffic controller in Lagos managing signals during rush hour. These tasks demand instant responses—delays could mean crop losses or traffic chaos. Edge computing processes data near its source, reducing reliance on distant cloud servers. In Nigeria, where internet connectivity is inconsistent and latency is high, edge nodes are a practical solution for reliable real-time applications.

# Understanding Edge Computing Basics

Edge computing moves data processing from distant cloud servers to local devices or small, nearby servers (“edge nodes”). These nodes—often compact units placed in mini data centers or telecom towers—contain processors, storage, and networking hardware designed for ultra-low latency.

Because data is processed locally, real-time applications like autonomous systems, telemedicine, or industrial automation receive responses in milliseconds rather than waiting for data to travel long distances to the cloud.

In Nigeria, with more than 100 million internet users and rapidly growing IoT adoption across agriculture, healthcare, and manufacturing, edge computing reduces network congestion and supports efficient, high-speed data handling across bandwidth-limited environments.

Edge computing load data shows the processing demand and resource utilization across edge nodes, for mobile phone operators, in Nigeria.

# Nigerian Telecom Edge Load EDA

The dataset used in this project is a collection of edge computing load data for mobile phone operators in Nigeria.

Visual exploratory analysis of the "nigerian-telecom-edge-computing-load-data" dataset to understand distributions of load, utilization, and categorical dimensions across Nigerian edge nodes

## Dataset
- Source: https://huggingface.co/datasets/electricsheepafrica/nigerian-telecom-edge-computing-load-data
- Format: Parquet (recommended)
- Rows ~ 250k, Columns ~ 14

The notebook automatically downloads the Parquet file from the Hugging Face Hub using `huggingface_hub`. No manual data download needed.

## Project Structure
- `notebooks/edge_load_status_eda.ipynb` — Main EDA notebook
- `requirements.txt` — Python dependencies
- `figures/` — Created at runtime when saving plots (optional)
- `prompts/` - Created to hold prompts used in project
- `reports/` - Created to hold the visualization reports

## Setup (Windows)
1) Create and activate a virtual environment
```
python -m venv .venv
.\.venv\Scripts\activate
```

2) Install dependencies
```
pip install -r requirements.txt
```

3) Launch Jupyter
```
jupyter lab
# or
jupyter notebook
```

4) Open `notebooks/edge_load_status_eda.ipynb` and run cells.

## What the notebook does
- Loads dataset from Hugging Face (tries Parquet)
- Overview: shape, dtypes, missing values, memory usage
- Numeric distributions: histograms and boxplots for utilization/throughput/latency/session metrics
- Categorical distributions: city, application, operator, load_status (+ top edge_node_id)
- Time-based patterns: hourly and day-of-week counts
- Correlation heatmap of numeric features
- Optional saving of figures to `figures/`

## Notes
- Internet access required to download dataset on first run.
- Requires `pyarrow` for Parquet reads.
- Timezone: dataset timestamps are in WAT context; analysis uses naive timestamps as provided.

## Operator-Level Conclusions Of The Analysis

- **High-load share varies slightly by operator**: 39.067% (MTN) to 39.523% (9mobile).
- **Peak high-load hours cluster in the evening**: 9:00–13:00 across operators.
- **Metrics that rise most from low→high**: active_sessions (~311.8%→319.0% increase), memory_utilization_percent (~59.7%→60.8% increase), cpu_utilization_percent (~58.9%→59.8% increase).
- **Recurring city hotspots**: Kano (3 ops), Lagos (1 ops).
- **Recurring application hotspots**: ar_vr (2 ops), iot_processing (1 ops).
