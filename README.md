# CASE Study: Analysing HealthCare in Power BI
**Performance, Benchmarks, and Dashboard**

### Description:
In this Power BI case study, explore a real-world dataset to uncover hospital efficiency insights for the fictional consulting firm HealthStat. Analyze factors impacting patient length of stay and cost, use DAX to create measures and visualizations, and build a comprehensive dashboard to communicate your findings—all while honing a range of Power BI skills.

## Healthcare Analysis with Power BI
Measure efficiency in Healthcare, quickly check the dataset content, get started with some initial EDA, and leverage DAX to create calculated measures and columns.

## :diamond_shape_with_a_dot_inside:	 FRAMEWORK FOR HEALTHCARE QUALITY
### SAFETY > EFFECTIVENESS > TIMELINESS > PATIENT-CENTERED > EQUITY > EFFICIENCY

## :open_file_folder: About the Dataset
- New York state-wide hospital discharge data for 2016.  
- Elective hip replacement surgery patients.
  - ### **Columns that are Focus of Analysis**
    
  - **length_of_stay**
  - **total_cost**
  - facility_id
  - age_group
  - patient_disposition
  - ccs_diagnosis_description
  - apr_severity_of_illness_description
  - apr_risk_of_mortality
 
 ## :brain: **Calculating special measures or columns using DAX** 

```
Average Cost per Discharge ALL =
CALCULATE([Average cost per Discharge],ALL())
```
```
Average Cost per Discharge =
DIVIDE(SUM(hospital_discharge[total_cost],[Total_discharge]))
```
```
Average LOS Days ALL =
CALCULATE([Average LOS Days], ALL())
```
```
Average LOS Days =
AVERAGE(hospital_discharges[length_of_stay])
```
```
% Var Average LOS Days =
VAR vAVG = [Average LOS Days]
VAR vAvgALL = CALCULATE([Average LOS DAYS],ALL())
RETURN
  (vAVG-vAvgALL)/vAVGALL
