# ML-Ops Playground

A machine learning operations (MLOps) project demonstrating MLflow integration for experiment tracking and model management using the Iris dataset.

## Project Structure

```
ml-ops-playground/
├── .dockerignore
├── .gitignore
├── Dockerfile.mlflow
├── Dockerfile.training
├── README.md
├── compose.yml
├── requirements.txt
└── training.py
```

## Prerequisites

- Docker and Docker Compose
- Python 3.9+
- MLflow
- scikit-learn

## Quick Start

1. Clone the repository:
```bash
git clone https://github.com/yourusername/ml-ops-playground.git
cd ml-ops-playground
```

2. Start the MLflow server and training service:
```bash
docker compose up --build
```

The services will:
- Start MLflow server on http://localhost:8080
- Execute the training script automatically

## Project Components

### MLflow Server
- Tracks experiments and metrics
- Stores model artifacts
- Accessible via web UI at http://localhost:8080

### Training Pipeline
- Uses scikit-learn's Iris dataset
- Implements Logistic Regression model
- Logs metrics, parameters, and model artifacts to MLflow

## Model Details

- **Algorithm**: Logistic Regression
- **Dataset**: Iris Classification
- **Metrics**: Accuracy
- **Parameters**:
  - solver: lbfgs
  - max_iter: 1000
  - multi_class: auto
  - random_state: 8888

## Environment Variables

- `MLFLOW_TRACKING_URI`: URI for MLflow tracking server (default: http://mlflow:8080)

## Development

To modify the training pipeline:

1. Update `training.py`
2. Rebuild and run containers:
```bash
docker compose up -d --build
```

## License

[Your License Here]

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request