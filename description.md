# 🌾 OptiCrop – Entity Relationship Diagram Documentation

## 📌 Project Overview

**OptiCrop** is an intelligent agricultural decision-support system designed to optimize crop production using soil analysis and machine learning techniques. The system assists farmers in selecting suitable crops based on environmental and soil conditions.

---

## 📖 Introduction

The Entity Relationship (ER) Diagram defines the database structure of the OptiCrop system. It illustrates the entities, attributes, primary keys, foreign keys, and relationships required to manage agricultural data, machine learning models, crop predictions, and recommendation reports.

The database is designed to ensure efficient data storage, maintain data integrity, and support intelligent crop prediction processes.

---

## 🗂 Main Entities

### 👤 User

Stores farmer and system user information.

### 🌱 SoilData

Maintains soil nutrient values and environmental parameters collected from agricultural fields.

### 🌾 Crop

Contains crop details, classifications, and descriptions.

### 📂 Dataset

Stores information about datasets used for training machine learning models.

### 🤖 MLModel

Represents the machine learning models used for crop prediction.

### 📊 Prediction

Stores prediction results generated from soil data and trained models.

### 📑 Report

Maintains recommendation reports and summaries generated from prediction results.

---

## 🔗 Relationships

* One user can submit multiple soil records.
* Each soil record produces a crop prediction.
* A crop may appear in multiple prediction results.
* One dataset can train multiple machine learning models.
* One model can generate many predictions.
* A prediction can produce multiple reports and recommendations.

---

## 🔑 Primary Keys

* User → user_id
* SoilData → soil_id
* Crop → crop_id
* Dataset → dataset_id
* MLModel → model_id
* Prediction → prediction_id
* Report → report_id

---

## 🔐 Foreign Keys

* SoilData.user_id → User.user_id
* Prediction.soil_id → SoilData.soil_id
* Prediction.crop_id → Crop.crop_id
* Prediction.model_id → MLModel.model_id
* Report.prediction_id → Prediction.prediction_id

---

## ✅ Conclusion

The ER Diagram provides a well-structured database design for the OptiCrop system. It establishes relationships among users, soil information, crops, machine learning models, predictions, and reports. This architecture enables efficient data management and supports data-driven agricultural decision-making for smart farming applications.

