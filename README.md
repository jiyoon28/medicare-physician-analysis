# Medicare Physician & Other Practitioners — EDA & ML

**Goal**  
Understand what drives **Avg_Mdcr_Pymt_Amt** (average Medicare payment) and build simple models to predict it, using a 50k-row sample for fast iteration.



## Dataset
- **Source:** [CMS Provider Data](https://data.cms.gov/provider-summary-by-type-of-service/medicare-physician-other-practitioners/medicare-physician-other-practitioners-by-provider-and-service)
- **Format:** CSV
- **Size:** Large (~millions of rows)

**Key features used**
- Numeric: `Tot_Srvcs`, `Tot_Benes`, `Tot_Bene_Day_Srvcs`, `Avg_Sbmtd_Chrg`
- Categorical: `Rndrng_Prvdr_Type`, `Place_Of_Srvc`
- (Avoid leakage): do **not** feed `Avg_Mdcr_Alowd_Amt`, `Avg_Mdcr_Stdzd_Amt` into the model



## Results Summary
- Skewed payments/charges: heavy right tail → log-scale visuals help.

- Strong drivers: utilization (Tot_Srvcs, Tot_Benes) and Avg_Sbmtd_Chrg; specialty/place matter.

- Models: Random Forest provided more realistic predictions than plain Linear Regression on raw target.


