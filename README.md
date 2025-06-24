# Required Assignment 11.1: What Drives the Price of a Car?

### Project Overview & Business Understanding
This project analyzes a large dataset of used vehicles to understand the key factors influencing car prices. By building a predictive model, we aim to provide a dealership with a data-driven tool to guide their pricing strategy and inventory acquisition, translating complex data into actionable business insights.

### Link to Jupyter Notebook
*   [Link to the complete analysis in the Jupyter Notebook]()

---

### Summary of Findings
The analysis of over 400,000 vehicle records identified a clear hierarchy of factors that determine a used car's value. Despite data quality issues like missing values and outliers—which were addressed during data cleaning—the model successfully pinpointed these key drivers.  

*   **Key Price Drivers (in order of importance):**
    1.  **Vehicle Age (Year):** The most significant factor.
    2.  **Mileage (Odometer):** Higher mileage consistently lowers value.
    3.  **Manufacturer & Vehicle Type:** Premium brands and popular body types (e.g., trucks) hold value better.
    4.  **Condition & Appearance:** "Excellent" condition and popular colors command higher prices.

*   **Model Insights:** The final model, a Polynomial Ridge Regression, achieved an **average prediction error (RMSE) of approximately $6,600**. This metric was chosen to penalize large, costly errors more heavily. The model's success confirms that car pricing is not linear and depends on the interaction between multiple features.

---

### Modeling Process
A rigorous modeling process was followed to ensure the results were robust and reliable.

*   **Data Processing:** The dataset was cleaned by handling missing values and removing outliers. New features like vehicle `age` were engineered to improve model accuracy.
*   **Regression Models Tested:** Multiple regression models were evaluated, including Linear, Ridge, Lasso, and Polynomial Regression.
*   **Validation & Tuning:** 5-fold cross-validation was used to validate model stability. A `GridSearchCV` was performed to find the optimal hyperparameters for the best-performing models.

---

### Actionable Recommendations for the Business
1.  **Use for Baseline Pricing:** Use the model's prediction as a data-driven starting point for pricing all vehicles.
2.  **Apply Expert Adjustments:** The model provides a baseline.
3.  **Factors:**  Factors contributing to the used car price in the following order of importance:

        - Age (How old the car is)
        - Odometer
        - fuel Gas type 
        - fuel other type sedan
        - cylinder types coupe 6 and 4
        - gas type pickup trucks

---

### Project Organization
*   `README.md`: This summary of findings and project structure.
*   `prompt_II.ipynb`: The main Jupyter Notebook containing all code, analysis, and visualizations.
*   `data/vehicles.csv`: The dataset used for the analysis.
