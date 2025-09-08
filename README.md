# Cancer Research: Drug Simulator

<img width="2240" height="1173" alt="pic_1_initial_screen" src="https://github.com/user-attachments/assets/e9246133-45c3-4309-aff6-c3a12ea12362" />

This interactive R-based Shiny application provides a comprehensive platform for cancer drug response analysis, combining pharmacological modeling with machine learning predictions to support clinical decision-making. The application integrates drug response curves, survival analysis, toxicity profiling, and patient-specific outcome predictions to facilitate evidence-based cancer treatment selection.

🔗 Live Application: https://dgalgom.shinyapps.io/cancer_research/

## Application Modules

### Response Analysis 📊
This module enables comprehensive evaluation of drug efficacy against specific cancer cell lines.
**How to use**:

  1. Select Drug: choose from the dropdown menu of available anticancer drugs
  2. Select Cell Line: pick the cancer cell line of interest from the available options
  3. Review Results: the interface displays (a) evidence-based clinical effect data, (b) fitted dose-response curves with IC50 values, (c) overall survival (OS) curves, (d) progression-free survival (PFS) curves, and (e) drug mechanism of action details.

**Interpretation**:

  - Dose-Response Curves: Lower IC50 values indicate higher drug potency
  - Survival Curves: steeper curves suggest better treatment outcomes
  - Mechanism of Action: provides biological context for observed responses

### Survival Analysis 📈
<img width="2240" height="1172" alt="pic_2" src="https://github.com/user-attachments/assets/3cf17039-9008-4e72-ada8-29423cf3a55e" />

This module performs patient stratification analysis based on clinical characteristics.
**How to use**:

  1. Select Patient Characteristics: choose relevant clinical parameters (e.g., tumor stage, patient age, biomarker status)  
  2. Generate Plots: the system automatically generates: (a) Kaplan-Meier survival curves for OS, and (b) Kaplan-Meier curves for PFS.

### Toxicity Profile
<img width="2235" height="1172" alt="pic_3" src="https://github.com/user-attachments/assets/3ba94db1-7fdc-48a7-b019-426490bb63fb" />

Comprehensive assessment of drug safety profiles and therapeutic windows. Plots showing **overall toxicity assessment**, and **organ-specific toxicity** (e.g., hepatotoxicity or cardiotoxicity).
The therapeutic window analysis visualizes the relationship between efficacy and safety, presenting the therapeutic index (i.e., quantitative measure of drug safety margin). 
Finally, a comparative analysis on Grade 3-4 toxicity is conducted between the selected drug vs. drug class averages.

**Interpretation**:
  - Higher therapeutic index: wide safety margin, more favorable risk-benefit profile
  - Grade 3-4 toxicity: severe adverse events requiring dose modification or discontinuation

### Machine Learning (ML) Comparison 🤖
<img width="2234" height="1159" alt="pic_4" src="https://github.com/user-attachments/assets/4a180c8d-40c0-452e-b297-0f453bf41b2a" />

Advanced machine learning module for predictive modeling and algorithm comparison.

**Primary Model**:
  - Random Forest Regressor: Primary algorithm for drug response prediction
  - Feature Importance: Identifies key predictors of treatment response
  - Cross-Validation: Ensures model robustness and prevents overfitting

**Model Comparison Features:**
Algorithm Benchmarking: Compare Random Forest against:

  - Support Vector Machines (SVM)
  - Gradient Boosting Models
  - Linear Regression

**Performance Metrics**:
  - R² (coefficient of determination)
  - RMSE (Root Mean Square Error)
  - MAE (Mean Absolute Error)

### Patient Prediction 🎯
<img width="2240" height="1167" alt="pic_5" src="https://github.com/user-attachments/assets/90fad821-5722-4b58-9632-a26bd44778f5" />

Personalized outcome predictions using fitted ML models.

**Input parameters**: age, sex, ECOG performance status, cancer stage, HRD status, MSI status, BRCA status, PD-L1 expression (%), and TMB score.
**Predictions generated**:

  - Drug response probability: likelihood of treatment response
  - Survival estimates: predicted OS and PFS
  - Risk stratification: patient assigment to risk categories

**Potential clinical applications**:

  - Treatment selection: identify most pormising therapeutic options
  - Patient counseling: provide evidence-based prognosis information
  - Clinical trial enrollment: screen patients for appropriate studies

### Comparative Analysis 🔄
<img width="2240" height="1169" alt="pic_6" src="https://github.com/user-attachments/assets/fe44c070-1f0f-4fcd-8b88-77224a8d05f1" />

Multi-drug comparison and comprehensive visualization module.

**Drug comparison features**:

  - Head-to-Head analysis: direct comparison of selected drug against similar agents
  - Response rate comparisons: efficacy across different cancer types
  - Survival outcome comparisons: OS and PFS across drug classes
  - Safety profile comparisons: toxicity patterns and severity

**Visualization components**:
<img width="1666" height="901" alt="pic_7" src="https://github.com/user-attachments/assets/582acbcb-5d90-4fc2-be1e-501948dd9f42" />

  - Response heatmaps: drug efficacy across all cell lines. The rows are the available drugs, the columns are the cancer cell lines, and the color gradient represents the response magnitude.
  - Survival heatmaps: survival outcomes across cancer types. The gradient values corespond to median PFS values.

#### Data sources
  - Publicly available cancer cell line databases
  - Clinical trial data repositories
  - Pharmacokinetic/pharmacodybamic databases
  - Genomic and proteomic datasets

#### Usage Guidelines
  1. Navigate to the application URL: https://dgalgom.shinyapps.io/cancer_research/
  2. Carefully read the 'About' module
  3. Begin with the 'Response Analysis' module to understand basic drug-cell line interactions
  4. Proceed through modules systematically for comprehensive analysis

#### Considerations
Individual-patient data (IPD) has been generated via IPD simulation techniques based on clinical literature on patient characteristics. Therefore, predictions on response and safety should not be taken into consideration for clinical decision-making. This application should complement, not replace, clinical judgment.

#### Citation
If you use this application in your research, please cite:

    Gallardo-Gómez, Daniel (2025). Cancer Research: Drug Simulator. A Drug Response Prediction Platform. Shiny Application. Available at: https://dgalgom.shinyapps.io/cancer_research/

#### Support and Contact
For technical support, feature requests, or collaboration inquiries:

  - **Email**: daniel.gallardogomez200@gmail.com
  - Github Issues: https://github.com/dgalgom/Cancer-research-Shiny-app/issues

#### Acknowledgments

  - Cancer research community for data contributions
  - Open-source R community for package development
  - Clinical collaborators for domain expertise validation
