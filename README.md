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
Explanation of data model:

Our model is based on the structure of a hypothetical vacation resort. The department entity is representative of a department (Finance, Human Resources, Food & Beverage, etc.) inside a resort location. Inside of this department, there are many employees, and this is represented by the one to many relationship we have placed between the Department and Employees entities.

There are also many employees inside of the hotel portion of the resort, which is why we established a one to many relationship between the Hotel and Employees tables as well.

There are two branches that come from the Hotel table. First, the Dining table represents all of the restaurants in the hotel. This table includes the revenue of the restaurant, the hours they are open, the dress code, and more. Restaurants in the Dining table have many reservations made by different guests of the resort, so there is a one to many relationship between the Dining entity and the DiningReservation entity.

On the other branch off of the Hotel table, there is the Room table. This simply contains all of the rooms inside each hotel. Because a guest can book many rooms, and rooms can be booked by many guests, we created an associative entity between Room and Guests called RoomReservation. The RoomReservation table allows the user to see which guests are in which room, when they check in, when they check out, and other information on the room.

There are various activities in the resort as well, and we’ve shown this by including an Activities table. The Activities table shows the price of the activity, its description, and the activity name. Guests may reserve many activities and activities can be reserved by many guests, so because of this we created an ActivityReservation table as the associative entity between Guests and Activity. ActivityReservation contains the activity time, the number of guests, the reservationID, and the guestID of the guest who registered for the activity. The resort offers a kids’ club which has a capacity, a contact email and phone number, and a rating. This is represented by the KidClub entity and its attributes. The kids’ club for the resort services the resort’s multiple hotels; therefore, there is a one-to-many relationship between the KidClub and Hotel entities.

Lastly, there is a transportation entity that represents the transportation services associated with the resort. The resort provides shuttles, bikes, buses, and a specialty limo service for guest transportation. The resort has also partnered with Uber and Lyft to offer rides to customers at a discounted rate. This is all reflected in the transportation entity that has a many to one relationship with the Hotel entity because the Hotel has many transporters, but each transporter is mapped to a certain hotel.

<img width="576" alt="Screenshot 2025-03-18 at 12 01 33 PM" src="https://github.com/user-attachments/assets/523be273-5900-4213-aae3-f3e2fd43f983" />

## Data Dictionary 
