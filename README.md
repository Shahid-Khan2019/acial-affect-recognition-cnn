# Facial Affect Recognition using CNN Baselines

## 📌 Project Overview

This project focuses on **Facial Affect Recognition using Deep Learning**. The system analyzes facial images and performs three affect-related prediction tasks:

- **Facial Expression Classification**
- **Valence Prediction**
- **Arousal Prediction**

Two pretrained Convolutional Neural Network (CNN) architectures were implemented and compared:

- **ResNet50**
- **EfficientNet-B0**

The project uses transfer learning with pretrained ImageNet weights and evaluates the models using multiple classification and regression metrics.

---

## 🎯 Objectives

The main objectives of this project are:

1. Classify facial expressions into **8 different classes**
2. Predict continuous **Valence** values
3. Predict continuous **Arousal** values
4. Compare the performance of ResNet50 and EfficientNet-B0
5. Analyze correctly and incorrectly classified facial images

---

## 🧠 Models Used

### ResNet50

- Pretrained on ImageNet
- Approximately 23 million parameters
- Used as a deep feature extraction backbone
- Final layer replaced with task-specific prediction heads

### EfficientNet-B0

- Pretrained on ImageNet
- Approximately 5.3 million parameters
- Lightweight and computationally efficient
- Used for comparison against ResNet50

---

## 🏗️ Model Architecture

Both models contain three prediction heads:

### 1. Expression Classification

- Output Classes: **8**
- Activation Function: **Softmax**

### 2. Valence Prediction

- Output: **1**
- Activation Function: **Tanh**

### 3. Arousal Prediction

- Output: **1**
- Activation Function: **Tanh**

---

## 🔄 Transfer Learning

Both ResNet50 and EfficientNet-B0 were initialized using **ImageNet pretrained weights**.

Transfer learning helps the models:

- Converge faster
- Reuse previously learned visual features
- Detect useful low-level patterns such as edges, textures, and shapes

The task-specific classification and regression heads were trained for the facial affect recognition task.

---

## ⚙️ Training Configuration

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Learning Rate | 0.0001 |
| Batch Size | 32 |
| Epochs | 10 |
| Dataset | 3,999 Facial Images |

---

## 📊 Performance Results

### Comparison of Models

| Metric | ResNet50 | EfficientNet-B0 |
|---|---:|---:|
| Accuracy | 0.3983 | **0.4350** |
| F1 Score | 0.3972 | **0.4336** |
| Cohen's Kappa | 0.3129 | **0.3546** |
| Valence RMSE | 0.4177 | **0.3960** |
| Valence Correlation | **0.5726** | 0.5546 |
| Arousal RMSE | 0.3804 | **0.3706** |
| Arousal Correlation | **0.3934** | 0.3678 |

### Key Observation

EfficientNet-B0 achieved better performance in most classification and regression metrics, including:

- Accuracy
- F1 Score
- Cohen's Kappa
- Valence RMSE
- Arousal RMSE

ResNet50 achieved slightly stronger correlation scores for:

- Valence
- Arousal

Overall, **EfficientNet-B0 provided a strong and lightweight baseline for this task**.

---

## 📈 Evaluation Metrics

The models were evaluated using:

### Classification Metrics

- Accuracy
- F1 Score
- Cohen's Kappa

### Regression Metrics

- RMSE (Root Mean Squared Error)
- Pearson Correlation

### Additional Affect Recognition Metrics

- SAGR (Sign Agreement)
- CCC (Concordance Correlation Coefficient)

---

## 📁 Project Structure

```text
facial-affect-recognition-cnn/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── facial_affect_recognition.ipynb
│
├── data/
│   ├── README.md
│   └── dataset_link.txt
│
├── results/
│   ├── training_graphs/
│   └── sample_predictions/
│
└── models/
```

---

## 💻 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/facial-affect-recognition-cnn.git
```

Move into the project directory:

```bash
cd facial-affect-recognition-cnn
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## 📦 Requirements

The project may require the following Python libraries:

```text
tensorflow
keras
numpy
pandas
matplotlib
scikit-learn
opencv-python
jupyter
```

> Update the `requirements.txt` file according to the exact libraries used in your `.ipynb` notebook.

---

## 🚀 Running the Project

1. Download the dataset.
2. Place the dataset inside the appropriate data directory.
3. Install all required dependencies.
4. Open Jupyter Notebook:

```bash
jupyter notebook
```

5. Open:

```text
notebooks/facial_affect_recognition.ipynb
```

6. Run the notebook cells sequentially.

---

## 🖼️ Dataset

This project uses a dataset containing **3,999 facial images** for facial affect recognition.

Due to potential GitHub file-size limitations, the dataset may not be included directly in this repository.

Dataset location/link should be added here:

```text
data/dataset_link.txt
```

---

## 📊 Results

The project includes:

- Training and validation performance analysis
- Comparison between ResNet50 and EfficientNet-B0
- Classification results
- Valence and arousal regression results
- Examples of correctly classified images
- Examples of incorrectly classified images

---

## 🔮 Future Improvements

Possible improvements include:

- Training for more epochs
- Hyperparameter tuning
- Data augmentation improvements
- Trying larger pretrained architectures
- Fine-tuning additional layers
- Using more training data
- Improving class balancing
- Deploying the model as a web application

---

## 👨‍💻 Author

**Shahid Ullah**

BS Data Science  
FAST-NUCES

---

## 📄 License

This project is intended for educational and research purposes.
