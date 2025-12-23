**/
Vehicle Rental System – SQL Query Explanations
This document explains the SQL queries written for the Vehicle Rental System database.
The database consists of three tables: user, vehicle, and bookings.

🔹 Query 1: JOIN
Objective
Retrieve booking information along with the customer name and vehicle name.

SQL Concepts Used
INNER JOIN

Explanation
This query joins the bookings table with the user and vehicle tables using foreign keys.
Each booking is linked to exactly one user and one vehicle.
The INNER JOIN ensures that only records with matching user and vehicle data are returned.

Output
Displays:

Booking ID

Customer name

Vehicle name

Rental start and end date

Booking status

🔹 Query 2: EXISTS
Objective
Find all vehicles that have never been booked.

SQL Concepts Used
NOT EXISTS

Subquery

Explanation
This query selects vehicles for which no matching record exists in the bookings table.
The NOT EXISTS clause checks each vehicle and excludes those that appear in any booking.

Output
Displays vehicles that were never booked, including:

Vehicle name

Type

Model

Registration number

Rental price

Availability status

🔹 Query 3: WHERE
Objective
Retrieve all available vehicles of a specific type (e.g., cars).

SQL Concepts Used
SELECT

WHERE

Explanation
This query filters vehicles based on availability status and vehicle type.
Only vehicles that are marked as available and match the given type are returned.

Output
Displays all available vehicles of the specified type.

🔹 Query 4: GROUP BY and HAVING
Objective
Find vehicles that have been booked more than two times.

SQL Concepts Used
GROUP BY

HAVING

COUNT()

Explanation
This query groups bookings by vehicle and counts how many times each vehicle has been booked.
The HAVING clause filters the grouped results and returns only those vehicles with more than two bookings.

Output
Displays:

Vehicle name

Total number of bookings

✅ Conclusion
These queries demonstrate the use of relational database concepts such as joins, subqueries, filtering, grouping, and aggregate functions to retrieve meaningful information from the Vehicle Rental System database.

🎤 Viva / Exam Short Explanations (Very Important)
🔸 Query 1 (JOIN)
This query uses INNER JOIN to combine bookings with users and vehicles, allowing us to display booking details along with customer and vehicle information.

🔸 Query 2 (EXISTS)
This query uses NOT EXISTS to find vehicles that do not appear in the bookings table, meaning those vehicles have never been booked.

🔸 Query 3 (WHERE)
This query retrieves vehicles based on specific conditions such as availability status and vehicle type using the WHERE clause.

🔸 Query 4 (GROUP BY & HAVING)
This query groups bookings by vehicle and counts them using COUNT(). The HAVING clause filters vehicles that have more than two bookings.

/**
