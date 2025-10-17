#Hospital Patient Sales Data Analysis 


Objective:
To build an interactive hospital analytics dashboard that provides deep insights into patient demographics, doctor performance, hospital operations, and financial metrics.
 The goal is to help hospital management monitor performance, optimize resources, and improve patient care through data-driven decisions.

Tools & Technologies Used
Power BI Desktop – Data modeling, visualization, DAX calculations


Power Query Editor – Data cleaning and transformation


SQL Server / Excel – Data source for loading hospital records


DAX Functions – For KPIs, measures, and custom insights



Dataset Overview
The dataset was designed to represent a real hospital environment and includes multiple entities:
Table
Description
Patients
Patient details, admission/discharge info, diagnoses, charges
Doctors
Doctor information, specialization, salary, and commission
Appointments
Appointment schedules with patients
Medicine
Medicine stock, usage, and sales trends
Finance
Billing, commission, and cost-revenue metrics


Dashboard Pages & Insights
1. Overview Page
Summary view of total patients, doctors, bills, and staff


Visuals for Stock vs Sales and Occupied vs Available Beds


Patient discharge trend line


KPI cards: Discharge %, Rating Score, Patient Count, Staff Count


Purpose: Gives hospital administrators a quick bird’s-eye view of overall performance.


2. Patient Page
Detailed patient profile with age, diagnosis, doctor-in-charge, and bed details


Monthly medicine tracking matrix


Patient charge-type breakdown (doctor fees, medicine, room, surgery, etc.)


Visuals showing medicine sales quantity


Purpose: To analyze patient-level treatment cost, medicine consumption, and diagnosis patterns.


3. Doctor Page
Doctor profile (specialization, salary, commission, patient spend)


KPIs: Commission Earned, Patient Spend, Commission Rate


Interactive “Commission Calculator” using Power BI parameters/sliders


Tabular view of patients treated, bills, and fees


Purpose: Helps HR/Finance teams assess doctor performance and revenue contribution.


4. Hospital Page
Displays patient age distribution


Bed occupancy status across General, ICU, Private wards


Surgery schedule tracker


Test results, notes, and medical observations per patient


Purpose: Provides operational visibility into hospital departments and resource utilization.


5. Finance Page
KPIs: Total Bills Amount, Doctor Salary, Doctor Commission %, Sales & Stock Qty


Comparative bar charts of Sales Qty vs Stock Qty for medicines and suppliers


Monthly medicine sales trend


Purpose: Enables financial monitoring of revenue, cost, and inventory efficiency.



Key DAX Measures Implemented
Total Bills Amt = SUM(Finance[Bills_Amt])


Discharge % = DIVIDE(SUM(Patient[Discharged]), COUNT(Patient[Patient_ID]))


Commission Earn = [Patient Spend] * [Commission Rate]


Available Beds = Total Beds – Occupied Beds


Medicine Trend = CALCULATE(SUM(Medicine[Sales_Qty]), FILTER(ALL(Medicine), …))



Business Impact
Enabled hospital management to track patient recovery and occupancy trends


Provided doctors and finance teams with transparent commission and spend visibility


Supported inventory management by comparing medicine sales vs stock levels


Delivered a data-driven performance framework improving patient satisfaction and cost efficiency



Design Highlights
Clean blue-white UI for clinical feel


Consistent KPI card styling and vector icons


Cross-page navigation via buttons and page tabs (Overview, Patient, Doctor, Hospital, Finance)


Tooltips and slicers for interactivity



