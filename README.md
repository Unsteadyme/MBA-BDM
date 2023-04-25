### HOTEL MANAGMENT SYSTEM
#### INTRODUCTION
A Hotel Management ER diagram is a visual representation of the data model used to manage hotel operations. It includes entities such as guests, reservations, rooms, employees, payments, and other key aspects of hotel management. The diagram helps hotel managers and developers understand the relationships between different entities in the system and can be used as a blueprint for developing a custom hotel management system. Overall, a Hotel Management ER diagram is a valuable tool for improving the efficiency and organization of hotel operations.

#### DOMINE ENTITY
1. Guest
2. Reservation
3. Room
4. Room Type
5. Room Status
6. Payment
7. Employee
8. Job Title
9. Department
10. Shift
11. Amenities
12. Event

These entities represent key aspects of hotel management and are used to store and manage data related to guests, reservations, rooms, employees, payments, and other important aspects of hotel operations. Together, they provide a comprehensive view of a hotel's operations and help to streamline processes, improve efficiency, and enhance the guest experience.

#### ATTRIBUTES FOR EACH ENTITY
1. Guest: guest_id, first_name, last_name, email, phone_number, address, nationality, date_of_birth, Age , passport_number
2. Reservation: reservation_id, guest_id, room_id, check_in_date, check_out_date, reservation_date, payment_status
3. Room: room_id, room_number, room_type_id, room_status_id, floor_number, description
4. Room Type: room_type_id, name, description, occupancy_limit, base_price
5. Room Status: room_status_id, name, description
6. Payment: payment_id, reservation_id, payment_method, amount, payment_date
7. Employee: employee_id, first_name, last_name, email, phone_number, department_id, job_title_id, shift_id, salary, hire_date
8. Job Title: job_title_id, title, description
9. Department: department_id, name, description
10. Shift: shift_id, start_time, end_time, description
11. Amenities: amenity_id, name, description
12. Event: event_id, name, description, date, time, location, organizer, attendees

#Guest
|G_ID| NAME          | ADDRESS                                |PHONE_NO               |E_MAIL                  | DOB            |NATIONALITY    |Age       |
|---:| ------------- |:--------------------------------------:| ---------------------:|------------------:|--------------------:|--------------:|---------:|
|008 | Rispa Maria   | 08/B block, Noida,Uttar Pradesh        | 7638926678            |rispam08@gmail.com      |19-03-2000      | Indian        | 23
|111 | Hari Krishnan | 11/H block, Coimbatore,                | 8897654253            |harikri0@gmail.com      |20-05-1999      | Indian        | 24
|107 | Mamta Rawat   | 20/C block, Lucknow, Uttar Pradesh     | 9450393599            |mamatra90@gmail.com     |03-01-2002      | Indian        | 21


#Reservation
|R_ID| Reservation_date     | Payment_Structure                      |Check_in_date          |Check_out_date     | 
|---:| -------------------- |:--------------------------------------:| ---------------------:|------------------:|
|101 | 19-04-2023           | 08/B block, Noida,Uttar Pradesh        | 20-04-2023            | 22-04-2023     
|102 | 21-04-2023           | 11/H block, Coimbatore,                | 22-04-2023            | 23-04-2023    
|103 | 24-04-2023           | 20/C block, Lucknow, Uttar Pradesh     | 25-04-2023            | 27-04-2023     


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
|e_ID| NAME          | Department                             |PHONE_NO               |Shift              |
|---:| ------------- |:--------------------------------------:| ---------------------:|------------------:|
|009 | Siddharth B   | HR Department                          | 7638926888            |Day   
|001 |Santhosh N     | Food Department                        | 9937654253            |Day and Night  
|006 | Sanskar G     | Housekeeping                           | 6450393566            |Night    


#Department
|D_ID| Department_name        | Description                            |
|---:| ---------------------- |:--------------------------------------:| 
|666 | HR Department          | 1000                                                        
|212 | Food Departnment       | 5000                                                     
|543 | Housekeeping           | 1000                                   


#Shift
|S_ID| Start_time        | End_time                               |Description          |
|---:| ----------------- |:--------------------------------------:| -------------------:|
|222 | 9am               | 5pm                                    | 19-04-2023                      
|111 | 6am               | 12am                                   | 21-04-2023                     
|333 | 9am               | 5pm                                    | 24-04-2023                        


#Amenities 
|Indoor_game_facilities | Wifi_facilities     | Playground       | Internet         |Gym       | Swimming_pool   |
|---------------------- |:-------------------:| ----------------:|------------------|----------|----------------:|
|Ludo                   | Available           |                  | 2                |Classic   | Available  
|Chess                  | Available           |                  | 4                |  Deluxe  | Available   
|Ball pool              | Available           |                  | 2                |Classic   | Available    


#Event
|e_id| Event_name    |Organizers                              | Location              |Attendees          |Date         | Time   |
|---:| ------------- |:--------------------------------------:| ---------------------:|------------------:|------------:|--------:|
|381 | marriage      | xyz                                    | gate 2                |Classic            | 20=03-2023  | 8
|114 | birthday      | abc                                    | Gate1                 |  Deluxe           | 22-03-2023  | 6
|411 | birthday      | qwe                                    | Gate1                 |Classic            |  23-03-2023 | 9
