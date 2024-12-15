# Road-Safety-Intelligence

## Challenge Addressed
This project investigates and analyzes patterns, causes, and consequences of motor vehicle collisions in New York City. The primary research questions include:
- What are the key factors contributing to motor vehicle collisions in NYC?
- Where are the most dangerous locations for collisions?
- When do most collisions occur?
- How can this information be utilized to improve road safety and reduce accidents?

---

## Data Profiling
The initial step focuses on understanding the characteristics and quality of the available data. Key activities include:
- Assessing data completeness, accuracy, and consistency.
- Identifying potential quality issues using tools like **Alteryx** and Python’s **Pandas Profiling** library.

---

## Data Integration and Staging
Three datasets—**Person**, **Vehicle**, and **Crashes**—were integrated from diverse sources and staged for analysis:
- **Vehicles** and **Person** datasets were extracted from NYC Open Data.
- **Crashes** data was retrieved from GCP BigQuery and integrated into a staging database.
This integration consolidates relevant information, providing a comprehensive view of vehicle collisions in NYC.

---

## Dimensional Modeling
A **dimensional data model** was designed to:
- Organize and structure data for analysis.
- Simplify complex data relationships, enabling easier extraction of insights.

---

## Data Cleaning and Integration
Data cleaning ensured accuracy and reliability by addressing missing, duplicate, and inconsistent values:
- **Null Values**: Replaced with “No Value Provided” across all dimensions, using `-99` as the surrogate key.
- **Travel Direction**: Standardized redundant directions to a consistent format.
- **Person Age**: Negative or unrealistic values replaced with `0`.
- **Vehicle Year**: Nulls and values outside the 1900–2023 range replaced with `9999`.
- **Vehicle Details**: Corrected discrepancies in `vehicle_type_code`, `vehicle_make`, `vehicle_model`, and `vehicle_year`.
- **Driver License Jurisdiction and State Registration**: Standardized to a two-character format; invalid inputs (e.g., special characters) were corrected or replaced with "Invalid Input."

---

## Key Findings and Significance

### 1. High-Risk Areas
- Identified specific intersections and locations with frequent collisions.
- Insights support city planners and traffic engineers in implementing safety measures and improving infrastructure.

### 2. Contributing Factors
- Revealed factors like weather, time of day, and driver behavior.
- Findings enable targeted education campaigns and enforcement strategies to enhance road safety.

### 3. Seasonal Trends
- Highlighted seasonal variations in collision rates.
- This allows authorities to allocate resources more effectively during high-risk periods.

### 4. Vehicle Type Analysis
- Identified collision patterns associated with specific vehicle types.
- Findings help guide regulations and safety measures for different vehicle categories.

### **Significance**  
These insights have the potential to drive evidence-based interventions that reduce collisions and improve road safety in NYC. By understanding the causes and patterns of collisions, policymakers, law enforcement, and city planners can collaborate to create safer streets, safeguarding residents and visitors alike.
