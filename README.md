# NYUAD-Team-12

## Setup Instructions

Follow these steps to set up the environment:

1. **Install `uv`**:
   First, install the `uv` package globally:
   ```bash
   pip install uv
   ```

2. **Create a Virtual Environment**:
   Use `uv` to create a virtual environment named `.venv`:
   ```bash
   uv venv
   ```

3. **Activate the Virtual Environment**:
   Activate the virtual environment using the following command:
   ```bash
   .venv\Scripts\activate
   ```

4. **Install Dependencies**:<br>
   There are two methods to do this<br>
   **Option 1: one easy command to use the .lock file**
   ```bash
   uv sync
   ```
   **Option 2**
   Second: using the requirements.txt file directly using pip or uv pip or even conda if you like:
   ```bash
   pip install -r requirements.txt
   ```

5. **Verify Installation**:
   Ensure all packages are installed correctly by checking their versions:
   ```bash
   pip list
   ```

You are now ready to use the environment!

---

## Quantum Support Vector Regression (Quantum SVR)

### Overview
This project demonstrates the use of Quantum Support Vector Regression (QSVR) and classical SVR models for population forecasting. The workflow involves data preprocessing, visualization, model training, evaluation, and forecasting using both classical and quantum approaches.

### Workflow

1. **Load and Process Data**:
   - The dataset is loaded from an Excel file.
   - Unnecessary columns are removed, and the date column is converted to a datetime format.
   - The data is indexed by the date column for time-series analysis.

2. **Create Training and Testing Datasets**:
   - Time-series datasets are created by using a sliding window approach to generate input sequences and corresponding target values.

3. **Visualize Data**:
   - The target variable (e.g., population) is visualized over time to understand trends and patterns.

4. **Split Data**:
   - The dataset is split into training and testing sets based on specified date ranges.

5. **Scale Data**:
   - Features and target variables are scaled using MinMaxScaler to normalize the data for better model performance.

6. **Train QSVR Model**:
   - The quantum kernel is defined using the `ZZFeatureMap`.
   - The QSVR model is trained using the quantum kernel.

7. **Evaluate the Model**:
   - The trained model is evaluated on both training and testing datasets.
   - Metrics such as Mean Squared Error (MSE) are calculated to assess model performance.

8. **Tune Parameters**:
   - Parameters such as `gamma`, `C`, and `epsilon` can be adjusted in the main execution section to optimize model performance.

9. **Train Classical and Quantum Models**:
   - Both classical SVR and QSVR models are trained using the prepared datasets.

10. **Test Models**:
    - Both models are tested on the testing dataset, and their predictions are compared.

11. **Forecasting**:
    - Future population values are forecasted using both models.
    - The results are visualized, highlighting the differences between classical and quantum approaches.

### How to Use
1. Modify the dataset path and column names in the main execution section to match your data.
2. Adjust the parameters in the main execution section to tune the models.
3. Run the notebook to execute the workflow, train the models, and generate forecasts.

### Implementation
All the code for the implementation is available in the `Quantum_SVR.ipynb` Jupyter notebook. Open the notebook to explore the workflow, train the models, and perform forecasting.

You can also open the `Quantum_SVR.ipynb` notebook in **Qbraid Lab** and run everything on the Qbraid cloud. This allows you to leverage Qbraid's quantum computing resources for executing the quantum model.

### Dependencies
- Qiskit
- Qiskit Machine Learning
- Scikit-learn
- Pandas
- Matplotlib
- OpenPyXL

### Notes
- Ensure that the versions of Qiskit and Qiskit Machine Learning are compatible.
- The quantum model requires a quantum simulator or quantum hardware for execution.

### Results
- The project provides a comparison between classical and quantum models for time-series forecasting.
- Forecasted values are visualized, and the performance of both models is evaluated.