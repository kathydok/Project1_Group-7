# Team 7 MIST Group Project 1 
## Team Name - Group 7 47114
## Team Members: 
- Aritra Mullick @amullickk
- Kathy Do @kathydok
- Carter Mixon @Cartermixon99
- Mary Grace Rudd @mgrudd 
- Sanaya Mohani @sanayamohani

## Problem Description:
In the modern healthcare industry, managing patient records, medical staff, appointments, prescriptions, billing, and insurance claims efficiently is critical for providing high-quality care. Our Hospital Management System (HMS) Database is designed to streamline these operations by implementing a well-structured relational database that ensures data integrity, accessibility, and efficient retrieval. The system tracks patients’ medical histories, doctor assignments, nurse care coordination, pharmacy inventory, and hospital facilities usage. It also handles billing and insurance processing, ensuring that all financial transactions related to patient care are accurately recorded and processed. By integrating multiple healthcare functions into a unified database, the system enables hospitals to improve workflow efficiency, minimize errors, and enhance patient experiences. This database also allows hospital administrators to gain business insights through structured queries, such as tracking appointment trends, monitoring doctor workloads, analyzing revenue from medical procedures, and managing inventory levels in the pharmacy. Our project focuses on designing, implementing, and optimizing this database, ensuring it meets real-world healthcare management needs while providing valuable analytics for hospital operations.

## Data Model
Explanation of the Hospital Management System Data Model

Our model is based on the structure of a hospital management system, focusing on patient care, medical staff coordination, facility management, billing, and pharmacy operations. The Patient entity represents individuals receiving medical care at the hospital, storing key details such as patient demographics, medical records, and contact information. Each patient is associated with one medical record, creating a one-to-one (1:1) relationship between the Medical_Records and Patient entities. These medical records store diagnoses, test results, prescriptions, and treatment plans.

Each medical record is assigned to a doctor, reflecting a one-to-many (1:M) relationship since a doctor can oversee multiple patients’ records, but each record is associated with only one doctor. Similarly, doctors handle multiple appointments, but each appointment is linked to a single doctor. The Appointments entity captures essential scheduling details, including appointment date, time, reason, and assigned hospital facility.

Hospital operations involve various hospital facilities, such as patient rooms, operation theaters, and diagnostic labs. Each appointment may require the use of a specific hospital facility, establishing a one-to-many relationship between the Hospital_Facilities and Appointments tables.

To ensure effective patient care, nurses are assigned to patients through the Care_Assignment entity, forming a many-to-many (M:M) relationship between Nurses and Patients. A nurse may be assigned to multiple patients, and a patient may receive care from multiple nurses throughout their treatment. Additionally, nurses are assigned tasks, which are recorded in the Tasks entity. Tasks may be linked to a specific appointment or part of general patient care responsibilities.

Pharmacy management is another critical aspect of the hospital system. The Pharmacy_Inventory entity tracks medication stock levels, expiry dates, and supplier details. Prescriptions are linked to Medical_Records and reference medications from the Pharmacy_Inventory, establishing a many-to-many relationship between medical records and medications.

Financial transactions are managed through the Billing_Insurance and Payments entities. Each appointment results in a billing record, creating a one-to-one relationship between Appointments and Billing_Insurance. Patients can pay their bills in multiple transactions, forming a one-to-many relationship between Billing_Insurance and Payments. The Payments table captures payment details, including amount, date, and method of payment.

<img width="571" alt="datamodel" src="https://github.com/user-attachments/assets/9e318007-e213-41ab-b693-cf5a03d02913" />

## Data Dictionary 
