# Automatic_Risk_Factor_and_System

# Model Using Instructions

## Overview
This project demonstrates a factor-based risk parity model using a combination of Python and web technologies for data analysis and visualization. Due to time and budget constraints, the system currently requires manual data downloads from platforms like Yahoo Finance and Wind for experiments.

## Workflow

### Step 1: Data Preparation
1. Manually download the required data from platforms such as Yahoo Finance or Wind.
2. Save the downloaded data into the `Risk_Factor_Model_Data` folder.

### Step 2: Code Execution
1. Open the `Risk_Factor_Model_Code` folder.
2. Update the file paths in the relevant code blocks to point to the data files in `Risk_Factor_Model_Data`.
3. Adjust the `factor_risk_parity_model` function as needed:
   - **Function Usage:**  
     ```python
     factor_risk_parity_model(dataframes["Asset"], dataframes["Factor"], "Factor_Risk_Parity", 1)
     ```
     - The last parameter in the function (`1` in the example above) specifies how often (in months) the portfolio weights are recalculated. You can freely modify this parameter to change the recalibration interval.
   - **Data Flexibility:**  
     The system allows for flexible inclusion of any number of asset and factor data, as long as they adhere to the format demonstrated in the dataset examples (`Risk_Factor_Model_Data`). Simply extend the dataset and update the paths in the script to incorporate additional data.
4. Run the Python scripts to process the data and generate the necessary outputs (e.g., factor exposure matrices, optimized weights).


### Step 3: Web Visualization
1. Move the output files generated from the Python scripts into the `Risk_Factor_Web_Demo` folder.
2. Navigate to the folder containing `index.html` in a terminal.
3. Start a local server by running the following command:
   ```bash
   python -m http.server 8000
   ```
4. Open your web browser and visit `http://localhost:8000` to view the interactive visualization of your results.

## Notes
- The system currently uses CSV files for data storage and processing.
- Future updates may include API integration for automated real-time data retrieval.
- Ensure all dependencies are installed before running the Python scripts. Dependencies include libraries like `Pandas`, `Numpy`, and `Scikit-learn`.
