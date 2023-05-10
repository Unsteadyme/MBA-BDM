#### Athul S 22121011
#### Kajal Singh 22121032

### HOTEL MANAGMENT SYSTEM
#### INTRODUCTION
A Hotel Management ER diagram is a visual representation of the data model used to manage hotel operations. It includes entities such as guests, reservations, rooms, employees, payments, and other key aspects of hotel management. The diagram helps hotel managers and developers understand the relationships between different entities in the system and can be used as a blueprint for developing a custom hotel management system. Overall, a Hotel Management ER diagram is a valuable tool for improving the efficiency and organization of hotel operations.


![image](https://github.com/Unsteadyme/MBA-BDM/assets/125996860/c0c0b89b-92f0-49c8-991c-42d645b6c0eb)

#### ATTRIBUTES FOR EACH ENTITY
1. Hotel: hotel_id, hotel name, hotel address(city, zipcode, state), hotel phone no
2. Guest: guest_id, first_name, last_name, email, phone_number, address, date_of_birth, Age 
3. Reservation: room_id, reservation_id, check_in_date, check_out_date, reservation_date, payment_structure
4. Room:  room_number, floor_number, room_type, occupancy_limit, base_price
5. Payment: payment_id, payment_method, amount, payment_date
6. Employee: employee_id, first_name, last_name, email, phone_number, department, job_title_id, shift
7. Job Title: job_title_id,salary, job_title_name, job_description, job requirement
8. Department: department_id, name, description
9. Shift: shift_id, start_time, end_time, description
10. Amenities: amenity_id, name, description
11. Event: event_id, name, description, date, time, location, organizer, attendees


#### DOMINE ENTITY
1. Hotel
2. Guest
3. Reservation
4. Room
5. Payment
6. Employee
7. Job Title
8. Department
9. Shift
10. Amenities
11. Event

These entities represent key aspects of hotel management and are used to store and manage data related to guests, reservations, rooms, employees, payments, and other important aspects of hotel operations. Together, they provide a comprehensive view of a hotel's operations and help to streamline processes, improve efficiency, and enhance the guest experience.



#Hotel
|H_ID| NAME          | ADDRESS                                          |PHONE_NO               |
|---:| ------------- |:------------------------------------------------:| ---------------------:|
|007 | TAJ           | 08/B block, LUCKNOW 226008 ,Uttar Pradesh        | 7638927678            
                                               
                                              
#Guest
|G_ID| NAME          | ADDRESS                                |PHONE_NO               |E_MAIL                  | DOB            |Age       |
|---:| ------------- |:--------------------------------------:| ---------------------:|-----------------------:|---------------:|---------:|
|008 | Rispa Maria   | 08/B block, Noida,Uttar Pradesh        | 7638926678            |rispam08@gmail.com      |19-03-2000      | 23
|111 | Hari Krishnan | 11/H block, Coimbatore,                | 8897654253            |harikri0@gmail.com      |20-05-1999      | 24
|107 | Mamta Rawat   | 20/C block, Lucknow, Uttar Pradesh     | 9450393599            |mamatra90@gmail.com     |03-01-2002      | 21


#Reservation
|R_ID| Reservation_date     | Payment_Structure                      |Check_in_date          |Check_out_date     | 
|---:| -------------------- |:--------------------------------------:| ---------------------:|------------------:|
|101 | 19-04-2023           | ONLINE                                 | 20-04-2023            | 22-04-2023     
|102 | 21-04-2023           | CASH                                   | 22-04-2023            | 23-04-2023    
|103 | 24-04-2023           | ONLINE                                 | 25-04-2023            | 27-04-2023     


#Room
|r_no| Floor_No.     | BASE_PRICE                             |OCCUPANCY_LIMIT        |ROOM_TYPE          | 
|---:| ------------- |:--------------------------------------:| ---------------------:|------------------:|
|301 | 2             | 1000                                   | 2                     |Classic     
|104 | 3             | 5000                                   | 4                     |  Deluxe   
|401 | 5             | 1000                                   | 2                     |Classic     


#Payment
|P_ID| Payment_method    | Amount                                 |Payment_date           |
|---:| ----------------- |:--------------------------------------:| ---------------------:|
|301 | Cash              | 1000                                   | 19-04-2023                      
|104 | Online            | 5000                                   | 21-04-2023                     
|401 | Online            | 1000                                   | 24-04-2023                        



#Employee
|e_ID| NAME          | Department                             |PHONE_NO               |Shift              | Job_title_id
|---:| ------------- |:--------------------------------------:| ---------------------:|------------------:|-------------:|
|009 | Siddharth B   | HR Department                          | 7638926888            |Day                |009
|001 |Santhosh N     | Food Department                        | 9937654253            |Day and Night      |001
|006 | Sanskar G     | Housekeeping                           | 6450393566            |Night              |006


#Job title
|jt_ID| Job_title_NAME          | Salary                                 |Job description        |Job requirement              | 
|----:| ----------------------- |:--------------------------------------:| ---------------------:|----------------------------:|
|009  | Siddharth B             | 25000                                  | 7638926888            |Day   
|001  |Santhosh N               | 65000                                  | 9937654253            |Day and Night  
|006  | Sanskar G               | 15000                                  | 6450393566            |Night    

#Department
|D_ID| Department_name        | Description                            |
|---:| ---------------------- |:--------------------------------------:| 
|666 | HR Department          | 1000                                                        
|212 | Food Departnment       | 5000                                                     
|543 | Housekeeping           | 1000                                   


#Shift
|S_ID| Start_time        | End_time                               |Description          |
|---:| ----------------- |:--------------------------------------:| -------------------:|
             


#Room type 
Guest_id                |Room size            | View             | Amenities        | Decor       | 
|---------------------- |:-------------------:| ----------------:|------------------|------------:|


#Event
|e_id| Event_name    |Organizers                              | Location              |Attendees          |Date         | Time   |
|---:| ------------- |:--------------------------------------:| ---------------------:|------------------:|------------:|--------:|










### ERP DIAGRAM
![ERD HOTEL MANAGMENT drawio (3)](https://user-images.githubusercontent.com/125996860/234365150-f12ca925-397e-42cc-a735-f6911e1f6e42.png)



