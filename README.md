# Medicare Provider EDA & ML

## Project Overview
This project analyzes the **CMS Medicare Physician & Other Practitioners — by Provider and Service** dataset to explore patterns in healthcare utilization, provider services, and Medicare payments.  
Using the CRISP-DM framework, the project includes **data cleaning, exploratory data analysis (EDA), and machine learning modeling** to predict Medicare payment amounts.


## Dataset
- **Source:** [CMS Provider Data](https://data.cms.gov/provider-summary-by-type-of-service/medicare-physician-other-practitioners/medicare-physician-other-practitioners-by-provider-and-service)
- **Format:** CSV
- **Size:** Large (~millions of rows)
- **Key Variables:**
  - `Rndrng_Prvdr_Type` — Provider specialty
  - `Place_Of_Srvc` — Place of service (facility/non-facility)
  - `Tot_Srvcs` — Total number of services
  - `Avg_Sbmtd_Chrg` — Average submitted charge amount
  - `Avg_Mdcr_Pymt_Amt` — Average Medicare payment amount *(Target variable)*


## Methodology (CRISP-DM)
1. **Business Understanding**
   - Identify key questions:
     - What features influence Medicare payment amounts the most?
     - How do utilization patterns vary by provider type and service location?
     - Can we accurately predict Medicare payment amounts?
   
2. **Data Understanding**
   - Load dataset, inspect structure, identify missing/categorical variables.
   - Generate summary statistics and visualizations.

3. **Data Preparation**
   - Handle missing values.
   - Encode categorical variables.
   - Scale numerical features if needed.

4. **Modeling**
   - Split data into train/test sets.
   - Train regression models (e.g., Linear Regression, Random Forest).
   - Evaluate model performance using metrics like MAE, RMSE, R².

5. **Evaluation**
   - Interpret feature importance.
   - Compare models.

6. **Deployment/Communication**
   - Publish findings in a non-technical blog post.
   - Share code and results on GitHub.



## Results Summary
- Key factors impacting Medicare payment amounts were identified, including **total services, provider type, and average submitted charge**.
- The trained model achieved an **R² score of X.XX** and an **RMSE of $X,XXX** on the test set.
- Regional and specialty-based variations in utilization patterns were observed.
