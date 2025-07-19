## Exploratory Data Analysis (EDA) Summary and Preprocessing Report

### **1. Summary of Findings from EDA**
- The dataset contained basic student records with `id`, `name`, and `score`.
- A quick inspection revealed missing values in the `score` column.
- Distribution of scores was moderately spread, with some outliers, and an average around the mid-range.
- Grouping by `name` showed multiple entries for some students, requiring aggregation for clearer insights.

### **2. Preprocessing Decisions**
- **Missing Values**: All missing scores were replaced with the **median** score to avoid skewing the distribution, as median is robust to outliers.
- **Normalization**: The `score` column was normalized (Z-score scaling) to ensure comparability across analyses and visualizations.
- **Aggregation**: For grouped statistics, scores were averaged per student name using `groupby()`. This provided a clean view of individual performance.

### **3. Rationale Behind Choices**
- **Median Imputation**: Median was preferred over mean because it resists the influence of extreme values (e.g., a student with an unusually low or high score).
- **Z-score Normalization**: This technique standardizes scores around a mean of 0 and standard deviation of 1, allowing fair comparison in any further analysis (e.g., modeling or clustering).
- **Descriptive Grouping**: Grouping and sorting by average scores provides insights into which students consistently perform better, which can guide further data exploration or interventions.

### **4. Conclusion**
These preprocessing steps laid the foundation for a clean and consistent dataset, suitable for further statistical or machine learning analysis. They reflect standard best practices for real-world data cleaning and exploratory analysis.

