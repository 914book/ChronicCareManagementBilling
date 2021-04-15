# Chronic Care Management Billing Automation Project
Healthcare Ambulatory Practice - active project

## Goal
To Automate Chronic Care Management (CCM) eClinicalWorks/third party monthly billing workflow processes with increased accuracy and efficiency.

### Reason 
* The Centers for Medicare and Medicaid Services (CMS) initiated the Chronic Care Management (CCM) program as a critical component of primary care that contributes to better health and care for individuals with multiple chronic conditions such as diabetes, high blood pressure and kidney diseseases. Once patient is enrolled in this program with their primary care provider, providers will create comprehensive care plan which allows patients to receive 24/7 access, continuity of care and comprehensive care management. CMS provides various financial incentives to primary care providers for additional time spent per patient and in turn reducing the cost of ER admissions and hospitalizations. 
* This program has two main components - clinical and billing. Clinical component involves patient identification, enrolling and care plan management. Billing component involves capturing time spent on monthly basis and finally create claims based on the minutes spent after number of exclusions such as hospice, transition of care and others.
* CMS has allowed the incentives but for providers must incoporate number of exclusions, documentations, minutes and billing (CPT codes) in order to get paid.
* The problem - disconnect with Electronic Health Records and complex CMS requirements and therefore, in order to verify accuracy, billing team has to perform  hours of manual verification.
* This project used Tableau to capture data from excel reports (which are downloaded from Electronic health records) and simplified billing processes with increased accuracy and efficiency.

### Description 
* Processes are divided into three sections as shown below:
* ![screenshot](https://github.com/914book/ChronicCareManagementBilling/blob/main/processes1.PNG)

### EHR Reports
* Various EHR based Monthly reports are auto scheduled to be dropped into Cloud based data storage.
  * CCM enabled patient list
  * CCM Not enabled patient list
  * CCM Not eligible patient list
  * For Exclusion - All patients billed for Home Health, TCM, SNF and Hospice
  * ALL CCM enbaled patients - PHM module - Practice added minutes list
  * All Telephone Encounters with Diagnosis codes for the month.
  * Third party vendor monthly billing report with minutes of services provided.
  
### Data Capture
  * pgAdmin
    * Table 1 - patient list 
    * Table 2 - CCM enabled key
    * Table 3 - exclusion list
    * Table 4 - PHM Module Minutes
    * Table 5 - TE for the month
    * Table 6 - Vendor Monthly billing report
    
 ### Data Visulization in Tableau
    * Dashboard - 
        * CCM enabled patient list with Telephone Encounters 
          * This list identifies patient list with non billable TE but billing team needs to count Minutes for CCM.
        * CCM Not enabled patient list with Telephone Encounters
          * This list identifies patient list with billable TE and billing team needs to generate claims differently.
        * CCM Exclusion list 
          * CMS does not allow CCM billing for certain exclusions such as Hospice, Nursing home, Home Health patients - so this list helps with exclusion.
        * Final Monthly CCM Billing list
          * This list generates final list with minutes and based on that - it also adds necessary CPT Codes.
        * Billing team gets this final list and they generate claims.
        * Additional Analytic reports for providers - identify trends and various useful insights for providers to improve patient care.
    

