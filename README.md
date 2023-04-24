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
