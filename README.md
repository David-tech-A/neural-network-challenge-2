# neural-network-challenge-2

# Employee Attrition and Department Prediction Model

This project implements a Deep Neural Network (DNN) to predict two outputs:
1. **Employee Attrition**: Whether an employee is likely to leave the organization (Yes/No).
2. **Employee Department**: The department to which the employee belongs.

The model uses shared hidden layers to process features and separate output layers for each prediction task.

---

## Table of Contents
- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Dataset Description](#dataset-description)
- [Model Architecture](#model-architecture)
- [Preprocessing Steps](#preprocessing-steps)
- [Results](#results)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)

---

## Overview
The objective of this project is to build a predictive model that helps HR teams:
- Understand which employees are at risk of leaving the organization.
- Classify employees into departments based on specific characteristics.

The project uses Python and TensorFlow to build, train, and evaluate a neural network model with high interpretability and performance.

---

## Technologies Used
- **Programming Language**: Python
- **Libraries**:
  - TensorFlow/Keras
  - Scikit-learn
  - Pandas
  - NumPy

---

## Dataset Description
The dataset includes employee-related features such as:
- Age
- Business Travel Frequency
- Job Satisfaction
- Distance from Home
- Department
- Attrition (Yes/No)

**Target Variables:**
1. `Attrition`: Binary classification (Yes/No)
2. `Department`: Multi-class classification

---

## Model Architecture
The model consists of:
1. **Input Layer**: Accepts the preprocessed features.
2. **Shared Hidden Layers**: Common layers that process the input data for both tasks.
3. **Separate Output Layers**:
   - `Attrition` output: A binary classification using a sigmoid activation function.
   - `Department` output: A multi-class classification using softmax activation.

Loss functions used:
- `Attrition`: Binary Crossentropy
- `Department`: Categorical Crossentropy

Optimizer: `Adam`

---

## Preprocessing Steps
1. **Data Cleaning**:
   - Handling missing values.
   - Removing duplicates.

2. **Feature Selection**:
   - Selected features such as Age, Job Satisfaction, Distance from Home, etc.

3. **Encoding**:
   - OneHotEncoding for categorical features (e.g., `OverTime`).

4. **Scaling**:
   - Applied StandardScaler to normalize numerical data.

5. **Splitting**:
   - Divided the data into training (80%) and testing (20%) sets.

---

## Results
### Evaluation Metrics
- **Department Accuracy**: 81.29%
- **Attrition Accuracy**: 53.40%

### Observations
- The model performs well for predicting the department but requires improvement for predicting attrition.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/David-tech-A/neural-network-challenge-2.git
   ```
2. Navigate to the project directory:
   ```bash
   cd attrition3000.ipynb
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the Jupyter Notebook or Python script:
   ```bash
   python train_model.py
   ```

---

## Future Improvements
- **Handle Imbalanced Data**:
  - Use SMOTE or class weights to address imbalance in the `Attrition` column.
- **Hyperparameter Tuning**:
  - Optimize the number of layers, units, and learning rates.
- **Additional Features**:
  - Engineer new features to improve predictive performance.
- **Alternative Architectures**:
  - Explore ensemble methods or transformer-based architectures.

---

## License
Na.

---

## Author
Developed by [David Melara](https://github.com/your-username).
