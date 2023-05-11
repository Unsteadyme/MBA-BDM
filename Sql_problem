
PROBLEM STATEMENTS


1) We need to determine the length of stay for guests below the age of 25 and guests above the age of 25 in order to analyze and compare their accommodation patterns.
By identifying the duration of their stays, 
we aim to gain insights into the preferences and behaviors of these two distinct age groups and potentially make informed decisions regarding our hospitality services.

CODE





CHART 


2) We need to retrieve the names of employees,
their job roles, and their salaries in the hotel management department. 
By obtaining this information, we aim to gain insights into the job roles and salary distribution within the hotel management team.

CODE:
SELECT Emp_name, job_role, salary_rs
FROM H_Employee
INNER JOIN job_title
ON H_Employee.job_id = job_title.job_id;



CHART



3) We need to obtain the shift descriptions for every employee in the hotel management department.
By retrieving this information, we aim to understand the specific shifts worked by each employee and gain insights into the scheduling and staffing patterns within the department.

CODE:
SELECT
    COUNT(CASE WHEN sh.s_description = 'Morning shift' THEN 1 END) AS morning_shift_count,
    COUNT(CASE WHEN sh.s_description = 'Evening shift' THEN 1 END) AS evening_shift_count,
    COUNT(CASE WHEN sh.s_description = 'Night Shift' THEN 1 END) AS Night_shift_count
FROM
    H_Employee emp
JOIN
    shift sh ON emp.shift_id = sh.shift_id;



CHART


4) We need to determine the amount of money paid by each guest to stay in the hotel managed by the hotel management team. 
By collecting this information, we aim to analyze the revenue generated from guest accommodations, evaluate pricing strategies, 
and understand the financial impact of guest bookings on the hotel's overall profitability. 

CODE:
SELECT
    gd.G_name,
    r.Base_price AS money_paid
FROM
    Guest_details gd
JOIN
    Room r ON gd.guest_id = r.guest_id;



CHART


5) We need to determine the count of payment methods used by guests in the hotel managed by the hotel management team. 
By gathering this information, we aim to analyze the distribution of payment methods utilized by guests during their stays.


CODE:
SELECT payment_method, COUNT(payment_method) AS count_of_payment_method
FROM payment
GROUP BY payment_method;



CHART



6) We need to determine the number of attendees for each event organized by the hotel management team. 
By obtaining this information, we aim to analyze the attendance patterns and popularity of various events hosted by the hotel. 



CODE:
SELECT Event_id, E_name, E_attendies
FROM H_event;


SELECT
  Room.Floor_no,
  COUNT(Room.guest_id) AS guest_count
FROM
  Room
JOIN
  Guest_details ON Room.guest_id = Guest_details.guest_id
GROUP BY
  Room.Floor_no;




CHART


7) We need to determine the guest count based on the view of the room in the hotel managed by the hotel management team.
By collecting this information, we aim to analyze the guest preferences for different room views and understand the demand for specific room types.



CODE:
SELECT room_view, COUNT(*) AS guest_count
FROM Guest_details
JOIN Room ON Guest_details.guest_id = Room.guest_id
JOIN Room_type ON Room.room_no= Room_type.Room_no
GROUP BY room_view;




CHART


8) We need to obtain the job descriptions for each employee in the hotel management department. 
By gathering this information, we aim to understand the roles and responsibilities of each employee within the hotel management team.


CODE:
SELECT Emp_name, job_description
FROM H_Employee
JOIN job_title ON H_Employee.job_id = job_title.job_id;



CHART



9) We need to identify the states from which guests are coming to the hotel managed by the hotel management team. 
By collecting this information, we aim to analyze the geographic distribution of our guests and understand their origin locations.


CODE:
SELECT state, COUNT(*) AS count
FROM Address
JOIN Guest_details ON Address.guest_id = Guest_details.guest_id
GROUP BY state;


SELECT gd.guest_id, gd.G_name AS guest_name, e.emp_id, e.Emp_name AS employee_name
FROM Guest_details gd
JOIN Phone_number pn ON gd.guest_id = pn.guest_id
JOIN H_Employee e ON pn.emp_id = e.emp_id
WHERE (pn.phone_number IS NOT NULL AND pn.phone_number_2 IS NULL)
   OR (pn.phone_number  IS NOT NULL AND pn.phone_number_2 IS NOT NULL);
SELECT gd.guest_id, gd.G_name AS guest_name, e.emp_id, e.Emp_name AS employee_name
FROM Guest_details gd
JOIN Phone_number pn ON gd.guest_id = pn.guest_id



CHART


10)


CODE


CHART
