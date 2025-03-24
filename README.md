# Bus-Booking-System
A Python-based bus ticket booking system that allows users to select travel details such as destination, bus, timing, pickup, and drop points. The system generates an OTP for verification and stores the booking information in a MySQL database. It provides a simple, interactive console interface for users to complete their booking securely.

Description of the Bus Ticket Booking System Code
This Python script implements a bus ticket booking system where users can book a bus ticket, select their travel details, and store the booking information in a MySQL database. The steps of the system are as follows:

1. Connecting to MySQL Database
The script connects to a local MySQL database called bus_booking using the mysql.connector module. It authenticates using the provided credentials (username: root, password: root123) to interact with the database and store the booking data.

2. User Input for Ticket Booking
The ticket_booking() function gathers various details from the user for booking:

User Details: The user is asked to input their name and phone number.

Travel Place: The user selects from five possible travel destinations. The options are presented in a list (e.g., "Chennai - Pune", "Chennai - Madurai", etc.), and the user is prompted to select a destination.

Bus Name: The user selects a bus operator for the trip from five available choices (e.g., "Kumaran Tours and Travels", "Praveen Travels", etc.).

Travel Time: The user selects a time slot for the trip, with available options such as "6AM - 9AM", "9AM - 12PM", etc.

Pickup Point: The user selects a pickup point from a list of options like "Koyambedu", "Tambaram", etc.

Drop Point: Similarly, the user selects a drop-off point from a list of options (e.g., "Swargate", "Mattuthavani", etc.).

Seat Booking: The user selects the number of persons traveling (e.g., "One Person", "Two Persons", "Three Persons").

Seat Number: The user selects their seat(s) from predefined options like "A1 A2", "B1 B2", etc.

3. OTP Generation and Verification
OTP Generation: A 4-digit OTP (One-Time Password) is randomly generated for the user.

OTP Verification: The user is prompted to enter the OTP sent to their mobile number. If the entered OTP matches the generated one, the booking continues. If the OTP is incorrect, the user is asked to try again.

4. Storing Booking Data in MySQL
After successful OTP verification, the booking details (name, phone number, travel place, bus name, travel time, pickup point, drop point, seat count, seat numbers, OTP) are inserted into the bookings table in the MySQL database.

The script executes an SQL INSERT statement to store the booking information.

5. Confirmation of Successful Booking
After the booking is successfully stored in the database, the system prints a confirmation message that the booking was successful.

The ticket details are displayed for the user to confirm their booking.

6. Closing Database Connection
After the booking process, the cursor and database connection are closed to ensure proper cleanup.

Key Points:
User Interaction: The script interacts with the user via the command line, requesting inputs for various booking options like travel place, bus name, and seat selection.

Random OTP: The system generates a random OTP to verify the user's identity, adding a layer of security to the booking process.

MySQL Integration: The booking details are stored in a MySQL database for future reference.

Error Handling: If the OTP entered by the user is incorrect, the system prompts the user to try again, ensuring proper validation.
