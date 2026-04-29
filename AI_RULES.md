# AI Development Rules - Fraud Detection System

## Tech Stack
- **Python 3.x**: The core language for backend logic and model inference.
- **Streamlit**: The primary framework for building the web interface and handling user interactions.
- **Pandas**: Used for all data manipulation, structuring inputs, and preprocessing.
- **Joblib**: The library for loading the serialized machine learning model pipeline.
- **Scikit-learn**: The underlying framework for the machine learning model and its preprocessing steps.
- **Jupyter Notebooks**: Used for exploratory data analysis (EDA) and model training workflows.

## Development Rules

### 1. UI & Frontend
- Use **Streamlit** (`st`) components exclusively for the user interface.
- Utilize `st.columns` for responsive side-by-side layouts and `st.divider()` for visual separation.
- Provide immediate user feedback using `st.error()` for fraudulent predictions and `st.success()` for legitimate ones.
- Keep the interface focused on the core task: transaction input and prediction output.

### 2. Data Handling
- Always wrap input data in a **Pandas DataFrame** before passing it to the model.
- Ensure DataFrame column names match the feature names expected by the pre-trained pipeline exactly.
- Validate numerical inputs (e.g., ensuring amounts are non-negative) using Streamlit's `min_value` parameter in input widgets.

### 3. Model Management
- Load the model pipeline (`.pkl`) at the top level of the script to ensure it is cached and not reloaded on every interaction.
- The model file should be treated as read-only by the web application; updates to the model should occur in the Jupyter environment.

### 4. Code Quality & Structure
- Adhere to **PEP 8** standards for Python code readability and structure.
- Use clear, descriptive variable names that correspond to the transaction features (e.g., `oldbalanceOrg`, `newbalanceDest`).
- If the main script exceeds 100 lines, refactor logic into helper functions or separate modules.

### 5. Icons & Visuals
- Use standard emojis or Streamlit's built-in icon support to enhance the visual experience.
- Maintain a clean, professional layout that prioritizes data clarity.