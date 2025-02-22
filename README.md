# Event Management System

## Project Description
This project is a Database Management System designed to efficiently manage event-related operations, including client bookings, task tracking, and attendance management.

## Team Members
- Sudhanshu
- Sindy
- Tharuni
- Marjan

## Problem Statement
The management of event logistics, bookings, and related services can become highly complex. This system aims to provide a structured approach to handling event management through a well-designed database solution.

## Importance of the Database
The database ensures efficient data organization, seamless tracking of bookings and tasks, and improved client and vendor relationships.

## System Requirements
- Manage clients, tasks, and bookings
- Track task progress and due dates
- Organize events and manage attendance

## Entity and Attribute Overview
The database includes key entities such as:
- **Locations**: location_id, city_name, location_type, max_occupancy, locations_client_id
- **Vendors**: vendor_id, vendor_name, contact_details, invoice_id
- **Invoices**: invoice_id, invoice_date_issued, status, vendor_id, client_id, payment_id
- **Events**: event_id, event_date, event_type, guest_count, description, location_id, client_id, feedback_id
- **Feedbacks**: feedback_id, rating, comment, client_id, event_id, staff_id
- **Staff**: staff_id, name, position, contact_details
- **Clients**: client_id, name, contact_details, location_id, invoice_id, event_id, feedback_id, payment_id, pending_bookings_id
- **Payments**: payment_id, amount, date, method, invoice_id, client_id
- **Tasks**: task_id, assigned_staff, event_id, deadline
- **Event Requests**: request_id, requesting_client_id, event_date, guest_count, approval_status

## Entity Relationships
### One-to-Many Relationships:
- Clients → Locations: A client may have multiple associated locations.
- Clients → Invoices: A client may have multiple invoices.
- Locations → Events: A location may host multiple events.
- Vendors → Invoices: A vendor may issue multiple invoices.
- Events → Feedbacks: An event may have multiple feedback entries.
- Events → Staff: Multiple staff members may be assigned to an event.
- Staff → Tasks: A staff member may have multiple tasks assigned.

### Many-to-Many Relationships:
- Locations ↔ Vendors: Multiple vendors may work at multiple locations.
- Clients ↔ Vendors: Multiple clients may engage with multiple vendors.

### One-to-One Relationships:
- Invoices ↔ Payments: Each invoice has one corresponding payment.
- Event Requests ↔ Events: Each event request leads to a single organized event.
- Event Requests ↔ Clients: Each event request is associated with a single requesting client.

## Conceptual & Logical Data Modelling
The project includes structured conceptual and logical data models to ensure robust database architecture.

## Database Implementation
The system includes UP and DOWN scripts for database migrations, allowing seamless changes to the schema.

## PowerApps Integration
The system may leverage PowerApps for improved user interaction and automation.

## Future Enhancements
- Automation of invoice generation and payment reminders
- AI-based event planning assistance
- Real-time event monitoring and reporting

## Installation & Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo-name.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the system:
   ```bash
   python main.py
   ```

## Contributors
- Sudhanshu, Sindy, Tharuni, Marjan

## License
This project is licensed under the MIT License.

