# :briefcase: CASE Study: Analysing HealthCare in Power BI :hammer_and_wrench:
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
 
##  :mag_right: Insights to Explore
  * Which Hospitals stand out with highest cost and LOS relative to the state average?
  * Which Hospitals stand out as biggest outliers overall?
  * Does larger surgical program size impact LOS and COST?

To answer these questions we will dive deeper into the dataset. Ask basic questions first  
What are the Total Discharges, and we can work from there. Total discharge per hospital, the total and average Length of Stay per Hospital  
Compare these hospitals and their total or average costs
 
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
```
## :chart_with_upwards_trend: DASHBOARD :bar_chart:
> **In this report page, I created page navigators to make this dashboard as user-friendly as possible.**   
![homepage](https://github.com/user-attachments/assets/d390051f-fda8-4086-8b8a-0e31f5fea1cc)
> Here, we can find basic KPIs but more important is the Key influencers, this visual is an AI driven tool that identifies the most significant factors influencing the selected outcome.   
![LosComparison](https://github.com/user-attachments/assets/8093247b-884c-470e-8436-a6f57aa1aaeb)
> Now, in this report page we can still see same visuals but I also incorporate the use of scatter chart. This helps the client understand the relationship between the Average Cost and the Average length of stay.
![Costcomparison](https://github.com/user-attachments/assets/492ea14a-b094-46af-9e24-4c9e75f36a02)
> In this final report is the Health service profile, how well or bad they do in terms of LOS, COST, severity of sickness and their mortality rate.
![Hospitalprofile](https://github.com/user-attachments/assets/0c9a3b92-5782-4dbd-b7f8-b2c3487c0908)


## :bulb: CONCLUSION
By connecting the data model in Power BI, I transformed raw data into actionable insights and leveraged exploratory analytics.   
I applied my DAX skills to create essential measures and built complex tables, which enabled me to identify key hospital performance outliers and understand the factors influencing patient length of stay and cost.  
I then developed a dashboard using the client's preferred color palette, ensuring a user-friendly, cohesive, and data-driven solution. This case study not only sharpened my technical skills but also deepened my understanding of the healthcare industry.
