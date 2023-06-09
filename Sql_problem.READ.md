
# PROBLEM STATEMENTS


###  1)
 We need to determine the length of stay for guests below the age of 25 and guests above the age of 25 in order to analyze and compare their accommodation patterns.
By identifying the duration of their stays, 
we aim to gain insights into the preferences and behaviors of these two distinct age groups and potentially make informed decisions regarding our hospitality services.

## TABLE
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/5b0cdc7b-abaf-4c8d-b055-de2c956ad3c5)




## GRAPH
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125997577/e7a7af90-0b8c-4de2-a124-f79d50200479)





### CODE
SELECT
    AVG(DATEDIFF(check_out, check_in_)) AS average_length_of_stay,
    CASE
        WHEN gd.G_age < 25 THEN 'Below 25'
        WHEN gd.G_age >= 25 THEN 'Above 25'
    END AS age_group
FROM
    Reservation res
    INNER JOIN Guest_details gd ON res.guest_id = gd.guest_id
WHERE
    gd.G_age < 25 OR gd.G_age >= 25
GROUP BY
    age_group;





### 2)
We need to retrieve the names of employees,
their job roles, and their salaries in the hotel management department. 
By obtaining this information, we aim to gain insights into the job roles and salary distribution within the hotel management team.


## TABLE
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/479437c2-86b6-4323-99a7-f10bb566f43c)



## GRAPH
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125997577/06f2a34e-0c49-4a2e-a67d-555d5fe00807)



### CODE:
SELECT Emp_name, job_role, salary_rs
FROM H_Employee
INNER JOIN job_title
ON H_Employee.job_id = job_title.job_id;


### 3)
We need to obtain the shift descriptions for every employee in the hotel management department.
By retrieving this information, we aim to understand the specific shifts worked by each employee and gain insights into the scheduling and staffing patterns within the department.


## TABLE
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/1ada7b9e-0f04-4a3a-83af-4eb6bb6ffe77)


## GRAPH
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125997577/a6376862-25a4-4e34-987d-29c85872e335)


 
#### CODE:
SELECT
    COUNT(CASE WHEN sh.s_description = 'Morning shift' THEN 1 END) AS morning_shift_count,
    COUNT(CASE WHEN sh.s_description = 'Evening shift' THEN 1 END) AS evening_shift_count,
    COUNT(CASE WHEN sh.s_description = 'Night Shift' THEN 1 END) AS Night_shift_count
FROM
    H_Employee emp
JOIN
    shift sh ON emp.shift_id = sh.shift_id;





# 4
We need to determine the amount of money paid by each guest to stay in the hotel managed by the hotel management team. 
By collecting this information, we aim to analyze the revenue generated from guest accommodations, evaluate pricing strategies, 
and understand the financial impact of guest bookings on the hotel's overall profitability. 

## TABLE
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/5dd384b6-a7b7-431f-a6b0-274e5aceb997)



## GRAPH
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125997577/29d7b1a0-07cb-4812-b7db-b8d268c7161b)

## CODE:
SELECT
    gd.G_name,
    r.Base_price AS money_paid
FROM
    Guest_details gd
JOIN
    Room r ON gd.guest_id = r.guest_id;

# 5)
 We need to determine the count of payment methods used by guests in the hotel managed by the hotel management team. 
By gathering this information, we aim to analyze the distribution of payment methods utilized by guests during their stays.

## TABLE
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/d2f95d46-f2de-4f43-b410-71ee2d4594db)



## GRAPH
 ![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/2a674d0f-8ceb-4c55-bada-6c4571512d41)
 
 
## CODE:
SELECT payment_method, COUNT(payment_method) AS count_of_payment_method
FROM payment
GROUP BY payment_method;







# 6)
We need to determine the number of attendees for each event organized by the hotel management team. 
By obtaining this information, we aim to analyze the attendance patterns and popularity of various events hosted by the hotel. 

## TABLE
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/59eec840-a824-4953-a7d2-b21b97e36869)



## GRAPH
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/c0ec2f5a-258e-4a72-9da2-3d31587e3bd2)

## CODE:
SELECT Event_id, E_name, E_attendies
FROM H_event;





# 7)
We need to determine the number of guests on each floor in the hotel managed by the hotel management team. 
By obtaining this information, we aim to analyze the distribution of guests across different floors and understand the occupancy patterns within the hotel.

## TABLE
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/33a8a36b-82f0-4644-b7b5-923869404a7e)



## GRAPH
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/897aa24e-75c1-457d-a3b8-cd8e4a842e01)

## CODE
SELECT
  Room.Floor_no,
  COUNT(Room.guest_id) AS guest_count
FROM
  Room
JOIN
  Guest_details ON Room.guest_id = Guest_details.guest_id
GROUP BY
  Room.Floor_no;












# 8)
We need to determine the guest count based on the view of the room in the hotel managed by the hotel management team.
By collecting this information, we aim to analyze the guest preferences for different room views and understand the demand for specific room types.

## TABLE
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/93112610-8ac7-4780-ad17-96381d049d71)

## GRAPH
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125997577/5cccb15c-922b-4aeb-9e69-492b6199e3fa)


## CODE:
SELECT room_view, COUNT(*) AS guest_count
FROM Guest_details
JOIN Room ON Guest_details.guest_id = Room.guest_id
JOIN Room_type ON Room.room_no= Room_type.Room_no
GROUP BY room_view;



## 9)
 We need to identify the states from which guests are coming to the hotel managed by the hotel management team. 
By collecting this information, we aim to analyze the geographic distribution of our guests and understand their origin locations.

## TABLE
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/c665345c-3f34-40df-9f47-6035eff0b078)


## GRAPH 
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125997577/7c529616-05f5-465b-a362-442a18c03471)

CODE:
SELECT state, COUNT(*) AS count
FROM Address
JOIN Guest_details ON Address.guest_id = Guest_details.guest_id
GROUP BY state;





# 10) 
We need to determine the number of guests and employees who have provided one or two phone numbers in the hotel management system.
By analyzing this information, we aim to understand the distribution of communication preferences among guests and employees. 

## Table

![image](https://github.com/Unsteadyme/MBA-BDM/assets/125997577/738dd481-692f-4706-9e8f-9178fb3819b7)

## graph
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125997577/bf006353-1972-4bcd-8e54-bb6194567606)

## CODE:
SELECT gd.guest_id, gd.G_name AS guest_name, e.emp_id, e.Emp_name AS employee_name
FROM Guest_details gd
JOIN Phone_number pn ON gd.guest_id = pn.guest_id
JOIN H_Employee e ON pn.emp_id = e.emp_id
WHERE (pn.phone_number IS NOT NULL AND pn.phone_number_2 IS NULL)
   OR (pn.phone_number  IS NOT NULL AND pn.phone_number_2 IS NOT NULL);
SELECT gd.guest_id, gd.G_name AS guest_name, e.emp_id, e.Emp_name AS employee_name
FROM Guest_details gd
JOIN Phone_number pn ON gd.guest_id = pn.guest_id






# 11 
 We need to obtain the job descriptions for each employee in the hotel management department. 
By gathering this information, we aim to understand the roles and responsibilities of each employee within the hotel management team.

## table 

Emp_name	job_description
Amit Patel	knowledge of food safety regulations
Smita Sharma	Experience in customer service
Rahul Singh	Experience in housekeeping preferred
Priya Gupta	Experience in maintenance
Anjali Mishra	knowledge of food safety regulations
![image](https://github.com/Unsteadyme/MBA-BDM/assets/125997577/37d3cc60-4818-4401-9fd3-8153c481634c)

## CODE:
SELECT Emp_name, job_description
FROM H_Employee
JOIN job_title ON H_Employee.job_id = job_title.job_id;





