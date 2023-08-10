**System Design: Cinema Seat Booking System**

**Overview:**
The Cinema Seat Booking System is designed to provide users with a seamless experience for selecting, purchasing, and receiving digital tickets for cinema seats. The system interacts with users, validates bank card information, checks seat availability, and generates digital tickets.

**Components:**

1. **User Interface (UI):**
   - Input Form: Collects user details, seat preference, and bank card information.
   - Display: Shows the purchase status and generated digital ticket.

2. **Main Application (`main.py`):**
   - Handles user interactions and coordination between various components.
   - Initializes user, seat, and card instances.
   - Calls functions to validate card, check seat availability, and generate tickets.

3. **Classes:**
   - **User:**
     - Attributes: name
     - Methods: buy(seat, card)

   - **Seat:**
     - Attributes: seat_id
     - Methods: get_price(), is_free(), occupy()

   - **Card:**
     - Attributes: type, number, cvc, holder
     - Methods: validate(price)

   - **Ticket:**
     - Attributes: user, price, id, seat_number
     - Methods: to_pdf()

4. **Databases:**
   - **cinema.db:** Stores seat information.
     - Table: Seat
     - Columns: seat_id, price, taken

   - **banking.db:** Stores bank card information.
     - Table: Card
     - Columns: type, number, cvc, holder, balance

5. **Sample PDF (`sample.pdf`):**
   - A generated digital ticket in PDF format.
   - Contains user's name, ticket ID, price, and seat number.

**Workflow:**
1. User interacts with the UI to provide details and bank card information.
2. Main application (`main.py`) initializes user, seat, and card instances.
3. Card validation is performed by checking the card database (`banking.db`).
4. Seat availability is checked using the seat database (`cinema.db`).
5. If card is valid and seat is available, the seat is occupied and a ticket is generated in PDF format.
6. Digital ticket is displayed to the user and saved as `sample.pdf`.

**Benefits:**
- Scalable: Can accommodate additional features like user authentication, payment gateway integration, etc.
- Modular: Each component (user, seat, card, ticket) can be extended independently.
- Database Integration: Utilizes SQLite databases for storing seat and card information.
- PDF Generation: Generates digital tickets in PDF format using the FPDF library.

This system design provides an organized structure for the Cinema Seat Booking System, highlighting the interactions between different components and their roles within the system.