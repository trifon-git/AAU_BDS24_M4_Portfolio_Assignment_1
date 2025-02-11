### 🏡 House Price Prediction - Deep Learning Assignment
This project applies deep learning techniques to predict house prices using a **neural network in PyTorch**. It includes **feature engineering, model training, hyperparameter tuning, and evaluation**. The repository is setup to run in Google Colab, just copy all files inside the files location of Google Colab.


---

### 📌 Steps in the Notebook
#### 1️⃣ **Preprocessing**
   - Handle missing values (imputation for numerical & categorical data).
   - Encode categorical features using `LabelEncoder`.
   - Standardize numerical features using `StandardScaler`.

#### 2️⃣ **Feature Selection & Analysis**
   - Compute correlation with `SalePrice` to identify important features.
   - Drop features with low correlation or high redundancy.

#### 3️⃣ **Feature Engineering**
   - Create new meaningful features (e.g., **Exterior Score, Basement Score**).
   - Encode qualitative features into numerical values.

#### 4️⃣ **Train-Test Split**
   - Split the dataset into **training** and **validation** sets.
   - Use **cross-validation** for better model evaluation.

#### 5️⃣ **Model Architecture in PyTorch**
   - Implement a **Multi-Layer Perceptron (MLP)** with:
     - 2-5 hidden layers (`[128, 64, 32]`, `[256, 128, 64, 32]`).
     - **ReLU activation** and **dropout layers**.
   - Train using **Adam optimizer**.

#### 6️⃣ **Training and Hyperparameter Tuning**
   - Experiment with **learning rates (`0.01`, `0.001`)** and **batch sizes (`32`, `64`)**.
   - Evaluate models using **RMSE, MAE, and R² Score**.

#### 7️⃣ **Model Evaluation**
   - Plot **loss curves** for training & validation.
   - Compute **final RMSE, MAE, and R² score** for model comparison.

### 📊 Model Performance
- **Best Architecture**: `[128, 64, 32]`
- **Optimizer**: `Adam`
- **Best RMSE**: `49,885`
- **Best MAE**: `32,727`
- **Best R² Score**: `0.676`
- **Best Hyperparameters**:
  - **Learning Rate**: `0.001`
  - **Batch Size**: `64`
  - **Activation Function**: `ReLU`
  
---


### 🔬 Future Improvements
- **Regularization**: Add **dropout layers (0.2 - 0.3)** to reduce overfitting.
- **Compare Optimizers**: Test **SGD with momentum** (`0.9`) vs. **Adam**.
- **Feature Engineering**:
  - Apply **log transformation** to `SalePrice` to normalize skewed prices.
  - Create **more interaction features** (e.g., `OverallQual * OverallCond`).
- **Hyperparameter Tuning**:
  - Experiment with **deeper architectures** (e.g., `[256, 128, 64, 32]`).
  - Adjust **learning rate decay** using a **scheduler**.


