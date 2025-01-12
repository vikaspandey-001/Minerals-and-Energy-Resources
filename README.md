# Minerals and Energy Resources Analysis

## Project Overview  
This project, titled **Minerals and Energy Resources Analysis**, focuses on analyzing stocks and flows of mineral and energy resources using a dataset based on the **System of Environmental-Economic Accounting (SEEA) Central Framework (2012)**. The analysis involves cleaning and preprocessing raw data, standardizing units, and creating an interactive Power BI dashboard to uncover key insights. 

## Dataset Description  
The dataset, named **Mineral and Energy Resources**, contains unprocessed data with 11,731 rows and multiple columns. The data provides insights into various mineral and energy resources, their classifications, and stocks and flows. Key columns include:  

1. **Reference Area**: Country of origin of resources.  
2. **Unit Measures**: Units in which the resources are recorded (e.g., Barrels, Tonnes, Cubic Meters).  
3. **Resource**: Types of minerals and resources analyzed.  
4. **Stocks and Flows**: Categories include:  
   - Closing stock  
   - Discoveries  
   - Discrepancies  
   - Downward reappraisals  
   - Extractions  
   - Opening stock  
   - Reclassifications  
   - Total additions/reductions to stock  
   - Upward reappraisals  
5. **Class**: Classification of resource types:  
   - Class A: Commercially recoverable resources.  
   - Class A_B: Commercial + Potentially Commercially recoverable.  
   - Class ATC: Includes all known deposits.  
   - Class B, B_C, C: Further classifications of recoverability.  
6. **Time Period**: Year in which resources were reported.  
7. **Observation Value**: Observed values for the resources.  
8. **Observation Status**: Status of the recorded observation.  
9. **Unit Multiplier**: Conversion factor for measurements.

## Steps Taken  

### 1. Data Cleaning and Preprocessing (Excel)  
- **Duplicate Check**: Removed duplicate columns and rows for a clean dataset structure.  
- **Unit Standardization**:  
  - Problem: Data contained inconsistent units (Barrels, Tonnes, etc.).  
  - Solution: Converted all units to a single standard: **Cubic Meters** using conversion formulas.  
  - Conversion Logic:  
    - 1 Barrel = 0.159 Cubic Meters.  
    - Volume (Cubic Meters) = Mass (Tonnes) ÷ Density (Tonnes/m³).  
  - Formula Used:  
    ```
    =IF(Unit="BBL_US", Value*0.159, IF(Unit="T", Value/VLOOKUP(Density, ConversionTable, 2, FALSE), Value))
    ```  
  - Created new columns: `Temp Unit` (temporary conversions) and `UNIT_M_CUBE` (final standardized values).  
- **Value-Only Dataset**: Generated a clean, formula-free sheet for Power BI import.  

### 2. Data Import (Power BI)  
- Imported the cleaned dataset into Power BI for advanced analysis and visualization.  

### 3. Visualization (Power BI Dashboard)  
Created an interactive dashboard with the following visualizations:  
1. **Total Unit by Stocks and Flows**: Clustered Column Chart.  
2. **Sum of Units by Resource**: Pie Chart.  
3. **Time Period Analysis**: Line Chart showing resource discoveries over time.  
4. **Country-wise Total Units**: Funnel Chart.  
5. **Stocks and Flows by Area and Class**: 100% Stacked Column Chart.  

## Insights Derived  
- **Regional Distribution**: Highlighted significant variations in resource distribution across countries.  
- **Stock Trends**: Identified key trends in resource stocks and flows over time.  
- **Resource Utilization**: Analyzed the relationship between resource classification and extraction levels.  

## Key Challenges  
1. **Unit Standardization**:  
   - Addressed discrepancies in unit measures with precise conversion formulas.  
2. **Handling Large Data**:  
   - Optimized data size for seamless Power BI processing.  

## Key Learnings  
- Advanced techniques for cleaning and preprocessing environmental datasets.  
- Proficiency in creating dynamic dashboards using Power BI.  

## Deliverables  
1. **Power BI Report File (.pbix)**:  
   - Interactive dashboard for resource analysis.  
2. **Project Documentation**:  
   - Comprehensive explanation of data processing and visualization steps.  
3. **Insights Summary**:  
   - Actionable insights for policymakers and environmental analysts.  

## Tools and Technologies  
- **Microsoft Excel**: Data cleaning and preprocessing.  
- **Power BI**: Data visualization and dashboard creation.  

## How to Use  
1. Access the project files via GitHub: [Github Link](https://github.com/vikaspandey-001).  
2. Explore the Power BI report file to interact with visualizations.  
3. Review project documentation for detailed steps and insights.  

## Acknowledgments  
- Dataset Source: [Mineral and Energy Resources Dataset](https://shorturl.at/fbepE).  
- Based on SEEA and UNFC standards.  

Connect with me on LinkedIn: [Vikas Pandey](https://www.linkedin.com/in/vikaspandey001/). Feedback and contributions are welcome!  
