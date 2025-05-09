# 🐦 Bird Species Classification using DenseNet121 🦜🦉🦅🦆

This project leverages the DenseNet121 architecture to classify bird species (Parrot, Eagle, Hornbill, Duck, Owl) using deep learning. The workflow includes data preparation, training, evaluation, and result visualization. The dataset is assumed to be a zip file containing shuffled images named with their class prefixes.

---
## 📌 Project Objective
The goal is to build a robust image classifier that can automatically identify different bird species using transfer learning with DenseNet121. The model is trained on preprocessed images and evaluated for accuracy, loss, mean average precision (mAP), and confusion matrix.
---
## 🧠 Files Explained
### 1. DataPreparation.py
Purpose: Extracts the zipped dataset, splits it into training/validation/test folders, and resizes/standardizes images to 224x224.

  Main Features:

- Automatically creates directories.

- Splits data based on given ratios (70% train, 20% validation, 10% test).

- Standardizes and resizes images using Pillow and NumPy.

### 2. DenseNet121.py
Purpose: Trains a DenseNet121 model using the prepared dataset.

  Main Features:

- Uses Keras and TensorFlow for model training.

- Includes data augmentation to improve generalization.

- Saves training graphs (accuracy/loss), predictions, and the trained model.

- Outputs training time, accuracy, loss, and confusion matrix.

- Calculates mean average precision (mAP) for performance evaluation.

### 3. DenseNet121Model.py
Purpose: Loads the trained model and evaluates its performance on the test set.

  Main Features:

- Uses the test data generator for batch evaluation.

- Displays a confusion matrix and classification report.

- Helps in validating the model after deployment or training.

### 4. KaggleDataSet.py
Purpose (optional placeholder): Can be used to download or handle datasets from Kaggle if needed.
---
## 🐦 Bird Classes
* Parrot

* Eagle

* Hornbill

* Duck

* Owl
  
---
## 📈 Outputs
- DenseNet121_Model/densenet121_model.h5 – Saved trained model.

- DenseNet121_Graph/accuracy_loss.png – Training/validation accuracy and loss plots.

- DenseNet121_Graph/sample_predictions.png – Sample model predictions.

- DenseNet121_Graph/confusion_matrix.png – Confusion matrix on the test set.

---

## 📚 Requirements

Install with:
```batch
pip install tensorflow numpy matplotlib pillow scikit-learn
```
---
## 🧪 How to Run
Prepare your dataset:

Place ShuffledData.zip in the correct path.

### 1.Run the data preparation:
```batch
python DataPreparation.py
```

### 2.Train the model:
```batch
python DenseNet121.py
```

### 3.Evaluate the model:
```batch
python DenseNet121Model.py
```
---
