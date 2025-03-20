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

<img width="576" alt="Screenshot 2025-03-20 at 11 08 33 AM" src="https://github.com/user-attachments/assets/08a0eb51-d025-4c50-a1db-143cddfa64e3" />


## Data Dictionary 
<img width="686" alt="pharmacy" src="https://github.com/user-attachments/assets/bd8caab4-4a71-42d6-b49a-600a27e811ae" />

![image](https://github.com/user-attachments/assets/9d4f0350-55f0-4679-b2d9-d55997634976)
<img width="602" alt="patient" src="https://github.com/user-attachments/assets/68866cf4-761d-4c0f-87f1-7967cb84dc5d" />
![image](https://github.com/user-attachments/assets/56f12504-6aa8-4585-a88e-768272feadf5)
<img width="607" alt="Appointments" src="https://github.com/user-attachments/assets/f19a20e7-7575-4a25-a864-9909342bdd79" />
![image](https://github.com/user-attachments/assets/cf77293f-1c1f-4bde-8a6f-4b30eb36a9dd)
![image](https://github.com/user-attachments/assets/806110a4-4fa6-450b-b268-89e7ad6b2fab)
![image](https://github.com/user-attachments/assets/effc9905-b8ff-42a9-a7e4-480e6c721ae6)
![image](https://github.com/user-attachments/assets/cbfee21c-e62b-492a-8b8f-8309f2cbf142)
![image](https://github.com/user-attachments/assets/e65f0661-6c9c-4565-9fc1-d9086b8ef0db)
![image](https://github.com/user-attachments/assets/8a3af286-692a-4b49-86bf-e8613f683f1b)
![image](https://github.com/user-attachments/assets/59a8bd0c-798d-492a-8b8d-e4f8fadb55c1)

## Queries

Description: Query 1 lists the number of times each medication has been prescribed in the hospital, along with the name of the medication. The results are ordered by the number of prescriptions in descending order, ensuring that the most frequently prescribed medications appear first.

<img width="1005" alt="query1" src="https://github.com/user-attachments/assets/1402aed0-d408-4b2c-9fa7-caf2c3f001c9" />

Managerial Justification: Query 1 allows hospital administrators, pharmacists, and doctors to analyze prescription trends and identify the most commonly prescribed medications. This information is useful for pharmacy inventory management, ensuring that high-demand medications are adequately stocked. Additionally, doctors can use this data to assess prescribing patterns and ensure appropriate medication use. Sorting the results in descending order makes it easier to prioritize the most frequently prescribed medications for supply chain planning and patient care optimization.

------------------------------------------------------------------------------------

Description: Query 2 lists the number of appointments each doctor has, along with the doctor's name. The results are ordered by the number of appointments in descending order.

<img width="1017" alt="query2" src="https://github.com/user-attachments/assets/adffffbd-1cde-4944-98e1-0dcdf11009ae" />

Managerial Justification: Query 2 allows administrators to see which doctors have the most appointments, which can help with workload distribution, scheduling efficiency, and resource allocation. If some doctors have significantly more appointments than others, adjustments can be made to ensure balanced patient care. Ordering the results in descending order makes it easier to identify the doctors with the highest patient load.

------------------------------------------------------------------------------------

Description: Query 3 calculates the average, maximum, and minimum payment amounts for each payment method, while also counting the total number of transactions. It filters payments to include only those associated with billing records that have been marked as 'Paid', ensuring the accuracy of financial reporting. The results are grouped by payment method, ordered by the highest average payment amount, and exclude methods with zero transactions.

![QUERY 3](https://github.com/user-attachments/assets/5be41f27-4021-45f5-95c7-a13f406bd398)

Managerial Justification: Query 3 allows hospital administrators and financial teams to gain deeper insights into payment trends and patient payment behavior. By analyzing the average, highest, and lowest payments per method, the hospital can identify which payment types contribute the most revenue. The inclusion of a transaction count ensures a better understanding of payment volume, helping in financial forecasting and policy adjustments. This query helps optimize billing operations, ensuring that the most effective payment methods are promoted and supported within the hospital's financial infrastructure.

------------------------------------------------------------------------------------

Description: Query 4 lists the nurse ID and nurse name for nurses who have not been assigned any tasks by filtering out those whose IDs appear in the Tasks table.

<img width="1014" alt="query4" src="https://github.com/user-attachments/assets/0d834c73-9347-4689-b273-59541d2a43e1" />

Managerial Justification:
Query 4 helps administrators identify nurses who are currently unassigned, which can assist in balancing workloads, improving efficiency, and ensuring that all staff members are effectively utilized. If some nurses are consistently left without tasks, it may indicate inefficiencies in scheduling or task assignment. Additionally, this query can help in workforce planning, ensuring that available nurses are distributed evenly across shifts and departments to maintain optimal patient care.

------------------------------------------------------------------------------------

Description: Query 5 retrieves a list of patients who do not have any scheduled appointments. It checks the Patient table and filters out patients whose patientID appears in the Appointments table, ensuring that only those without upcoming or past appointments are included.

<img width="1015" alt="query5" src="https://github.com/user-attachments/assets/6f7d96d7-0386-4225-8353-3ef0bba00682" />

Managerial Justification: Query 5 allows hospital administrators and healthcare providers to improve patient engagement and follow-up care. By identifying patients who have not scheduled appointments, the hospital can proactively reach out to ensure necessary medical check-ups, follow-up visits, or preventive care appointments are arranged. This query supports better patient retention, improved health outcomes, and enhanced hospital-patient relationships by ensuring no patient is overlooked.

------------------------------------------------------------------------------------

Description: Query 6 retrieves the facility ID, room number, and room type for all hospital rooms that are currently available by filtering the Hospital_Facilities table where availability is marked as 'Available.'

<img width="1017" alt="query6" src="https://github.com/user-attachments/assets/f45b9336-76f6-4daa-b60a-67457d94d950" />

Managerial Justification: This query is useful for hospital administrators and staff to quickly identify which rooms are unoccupied and ready for new patients. It aids in efficient patient admission, transfer planning, and resource management. By knowing the available room types, hospitals can ensure that patients receive appropriate care in specialized units, such as ICU, maternity, or emergency rooms, without unnecessary delays.

------------------------------------------------------------------------------------

Description: Query 7 identifies doctors who have seen patients (handled appointments) but have not prescribed any medications. It does this by joining the Doctor table with the Appointments table while filtering out doctors who have documented prescriptions in the Medical_Records table. The query ensures that only doctors with more than two appointments are included, helping focus on those actively seeing patients.

<img width="1017" alt="query7" src="https://github.com/user-attachments/assets/8649bbd7-f6d7-40f4-836e-ddcb072ec112" />

Managerial Justification: Query 7 helps hospital administrators optimize doctor workload and integration into the hospital system. By identifying doctors who are seeing patients but not prescribing medications, the hospital can assess whether these doctors are specialists (e.g., surgeons, therapists) who do not typically prescribe drugs, new doctors who may need training, or physicians whose roles need further evaluation. The results are sorted by the number of appointments in descending order, making it easier to prioritize doctors with high patient interaction but no prescriptions.

------------------------------------------------------------------------------------

Description: Query 8 retrieves doctors who have attended at least one appointment but have prescribed medication in less than half of them. It calculates each doctor's total appointments and the number where prescriptions were issued, filtering for those with a prescription rate below 50%. Results are sorted by total appointments in descending order to highlight the most active doctors first.

![QUERY8](https://github.com/user-attachments/assets/d6bb237e-3c10-486c-afe0-837366d19b6a)

Managerial Justification: Query 8 helps hospital administrators assess prescribing patterns and identify specialists, new doctors, or underutilizing physicians. It supports resource allocation, training needs, and policy adjustments, ensuring appropriate medical care. Sorting by appointment count prioritizes doctors with the highest patient interactions for review.

------------------------------------------------------------------------------------

Description: Query 9 retrieves patients who have received at least one diagnosis. It counts the number of diagnoses recorded in the Medical_Records table for each patient and includes only those with one or more diagnoses. The results are grouped by patient and display their total diagnosis count.

![QUERY9](https://github.com/user-attachments/assets/7ffd0079-d9b9-40b7-ae6f-d6494c27cb54)

Managerial Justification: Query 9 helps hospital administrators and medical staff monitor patient health trends by identifying individuals with documented conditions. It aids in tracking chronic illnesses, ensuring follow-up care, and optimizing resource allocation for high-need patients. By highlighting diagnosed patients, the hospital can improve treatment planning and proactive patient engagement.

------------------------------------------------------------------------------------

Description: 
This query retrieves insurance providers with pending payments, calculating the total number of transactions, total pending amount, and average pending amount for each. It filters for specific providers (Medicare, Molina, and Aetna) and ensures that only those with at least one transaction are included. Results are sorted by total pending amount in descending order to highlight the largest outstanding balances.

![Screenshot 2025-03-20 at 12 21 18 PM](https://github.com/user-attachments/assets/b2e1d5e4-d62f-49a2-96c9-3942911b17d4)

Managerial Justification:
This query helps hospital financial teams monitor and manage outstanding insurance payments. By identifying providers with high pending amounts, administrators can prioritize follow-ups, streamline reimbursement processes, and improve cash flow management. Sorting by the highest pending balances ensures that the most critical cases receive attention first.

------------------------------------------------------------------------------------


<img width="679" alt="image" src="https://github.com/user-attachments/assets/1cf89473-b315-4b67-9313-e9bdfd052292" />
