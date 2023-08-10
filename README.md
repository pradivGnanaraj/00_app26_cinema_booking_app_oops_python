# Cinema Seat Booking System

This Python application simulates a cinema seat booking system. Users can select a seat, purchase a ticket, and receive a digital ticket in PDF format.

## Features

- Users can select and purchase cinema seats.
- Valid bank card information is required for purchasing.
- Digital tickets are generated in PDF format.

## Requirements

Ensure you have the following dependencies installed:

```bash
pip install fpdf
```

## Usage

1. Run the `main.py` file to start the application.
2. Enter your details as prompted:
   - Your full name
   - Preferred seat number
   - Card type (e.g., Visa, MasterCard)
   - Card number
   - Card CVC
   - Card holder name

3. The system will attempt to validate your card and purchase the selected seat.
4. If successful, a digital ticket (PDF) will be generated and saved as `sample.pdf`.
5. The ticket includes your name, ticket ID, price, and seat number.

## Files

- `main.py`: The main application file. Run this to use the cinema seat booking system.
- `User`: Represents a user who can purchase cinema seats.
- `Seat`: Represents a cinema seat that users can book.
- `Card`: Represents a bank card required to finalize seat purchases.
- `Ticket`: Represents a cinema ticket purchased by a user. Generates a digital ticket in PDF format.
- `cinema.db`: SQLite database containing seat information.
- `banking.db`: SQLite database containing bank card information.
- `sample.pdf`: Example generated digital ticket.
- `requirements.txt`: Lists required Python dependencies.

## System Architecture

The application follows a simple system architecture:

1. Users provide their information.
2. The system validates the user's bank card.
3. If valid, the system checks if the selected seat is available.
4. If available, the seat is booked, and a digital ticket is generated in PDF format.

## Enhancements

- User authentication for secure seat purchases.
- Online payment gateway integration.
- Improved error handling and feedback for users.

Feel free to contribute to this project and add more features!

**Note**: This application is for educational purposes and does not perform real transactions.