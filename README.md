# Iris Flower Classification API

## Overview

This project demonstrates the end-to-end deployment of a Machine Learning model using FastAPI and Docker. A Random Forest Classifier is trained on the Iris dataset and exposed through a RESTful API for real-time predictions.

The project showcases essential MLOps and deployment concepts, including model training, API development, inference endpoints, containerization, and production-ready project organization.

Developed as part of the **Interspark AI/ML Internship Program**.

---

## Project Objectives

* Train a machine learning classification model.
* Build REST API endpoints for model inference.
* Deploy the model using FastAPI.
* Containerize the application using Docker.
* Demonstrate practical ML deployment workflows.

---

## Key Features

* Machine Learning Model Training
* FastAPI-Based REST API
* Real-Time Prediction Endpoint
* Interactive Swagger Documentation
* Docker Containerization
* JSON Request & Response Support
* Production-Ready Project Structure

---

## Dataset Information

### Iris Flower Dataset

The Iris dataset is a widely used machine learning benchmark dataset containing measurements of iris flowers from three species.

### Features

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

### Target Classes

* Setosa
* Versicolor
* Virginica

### Dataset Statistics

| Property | Value                      |
| -------- | -------------------------- |
| Samples  | 150                        |
| Features | 4                          |
| Classes  | 3                          |
| Task     | Multi-Class Classification |

---

## Machine Learning Model

### Algorithm

Random Forest Classifier

### Why Random Forest?

* High Accuracy
* Robust Against Overfitting
* Easy Interpretation
* Excellent Performance on Small Datasets

### Training Pipeline

1. Load Dataset
2. Data Splitting
3. Model Training
4. Model Evaluation
5. Model Serialization
6. API Deployment

---

## API Endpoints

### Home Endpoint

GET /

Returns API status.

Example Response:

```json
{
  "message": "Iris Classification API Running"
}
```

---

### Prediction Endpoint

POST /predict

Predicts the iris flower species based on input measurements.

Example Request:

```json
{
  "sepal_length": 5.1,
  "sepal_width": 3.5,
  "petal_length": 1.4,
  "petal_width": 0.2
}
```

Example Response:

```json
{
  "prediction": "Setosa"
}
```

---

## Local Setup

### Clone Repository

```bash
git clone <repository-url>
cd Iris-Classification-API
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Train Model

```bash
python train_model.py
```

Output:

```text
Model saved successfully!
Location: Model/iris_model.pkl
```

---

## Run API

```bash
uvicorn app:app --reload
```

Open:

```text
http://127.0.0.1:8000/docs
```

Swagger UI provides interactive API testing.

---

## Docker Deployment

### Build Image

```bash
docker build -t iris-api .
```

### Run Container

```bash
docker run -p 8000:8000 iris-api
```

Access:

```text
http://localhost:8000/docs
```

---

## Project Structure

```text
Iris-Classification-API/
│
├── Model/
│   └── iris_model.pkl
│
├── Screenshots/
│   ├── swagger_ui.png
│   └── prediction_result.png
│
├── app.py
├── train_model.py
├── requirements.txt
├── Dockerfile
├── sample_request.json
├── README.md
└── Task3_Report.pdf
```

---

## Screenshots

The repository includes:

* Swagger API Documentation
* Successful Prediction Example
* Project Structure
* Deployment Demonstration

---

## Learning Outcomes

This project demonstrates practical understanding of:

* Machine Learning Deployment
* FastAPI Development
* REST API Design
* Model Serialization
* Docker Containerization
* Production Deployment Workflows

---

## Future Enhancements

* Cloud Deployment
* CI/CD Integration
* Kubernetes Deployment
* Model Monitoring
* Authentication & Security
* Database Integration

---

## Internship Information

Program: Interspark AI/ML Internship Program

Domain: Artificial Intelligence & Machine Learning

---

## Author

Yogendra

B.Tech – Artificial Intelligence & Machine Learning

Narasimha Reddy Engineering College

---

## License

This project is developed for educational, research, and internship submission purposes.
