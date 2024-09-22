# Event Management System

## Overview
This project is an **Event Management System** implemented using **SQL** in **MySQL**. The system allows for the management of various aspects related to events, including organizers, attendees, sponsors, tickets, and feedback.

## Database Structure
The database consists of the following tables:

- **Event**: Stores details about events, including name, description, dates, and organizer.
  - Fields: `EventId`, `EventName`, `Description`, `StartDate`, `EndDate`, `OrganizerID`

- **Location**: Contains information about event venues.
  - Fields: `LocationID`, `VenueName`, `City`, `State`, `Capacity`, `EventId`

- **Organizer**: Manages organizer details.
  - Fields: `OrganizerID`, `FirstName`, `LastName`, `CompanyName`

- **OrganizerPhoneNum**: Stores phone numbers of organizers.
  - Fields: `Organizerphonenum1`, `Organizerphonenum2`, `OrganizerID`

- **OrganizerEmail**: Manages email addresses for organizers.
  - Fields: `OrganizerEmail1`, `OrganizerEmail2`, `OrganizerID`

- **EventType**: Defines types of events.
  - Fields: `EventType`, `EventTypeName`, `Description`, `EventId`

- **Attendee**: Holds attendee information.
  - Fields: `AttendeeID`, `FirstName`, `LastName`, `FeedbackID`

- **Attendee_PhoneNum**: Stores phone numbers for attendees.
  - Fields: `PrimaryNum`, `SecondaryNum`, `AttendeeID`

- **Event_Attendee**: Associates attendees with events.
  - Fields: `AttendeeID`, `EventId`

- **Ticket**: Manages ticket information for events.
  - Fields: `TicketID`, `TicketType`, `PurchaseDate`, `Price`, `EventId`, `LocationID`, `AttendeeID`

- **Sponsor**: Stores sponsor details.
  - Fields: `SponsorID`, `SponsorName`, `ContactPerson`, `Email`, `ContactNumber`

- **Event_Sponsors**: Associates sponsors with events.
  - Fields: `EventId`, `SponsorID`

- **Speaker**: Manages speaker information.
  - Fields: `SpeakerID`, `SpeakerName`, `ContactPerson`

- **Speaker_Email**: Stores email addresses for speakers.
  - Fields: `Email1`, `Email2`, `SpeakerID`

- **Event_Speaker**: Associates speakers with events.
  - Fields: `EventId`, `SpeakerID`

- **Task**: Manages tasks related to event organization.
  - Fields: `TaskID`, `Description`, `Status`, `OrganizerID`

- **Feedback**: Stores feedback related to events.
  - Fields: `FeedbackID`, `Rating`, `Comments`, `SpeakerID`

## Features
- **Event Management**: Add, update, and manage event details, including dates and organizers.
- **Attendee Management**: Register attendees, track feedback, and manage attendee-related information.
- **Ticketing System**: Handle ticket purchases, types, and associations with events and attendees.
- **Organizer and Sponsor Management**: Manage details about event organizers and sponsors.
- **Speaker Management**: Track speakers, their details, and their association with events.

## Getting Started
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/event-management-system.git
    cd event-management-system
    ```

2. **Set Up MySQL**: Ensure you have MySQL installed and running. Create the `phase3` database using the provided SQL script.

3. **Execute the SQL Script**: Run the SQL script in your MySQL environment to create the database tables.

4. **Manipulate Data**: Use SQL queries to insert, update, delete, and retrieve data from the database.

## Future Enhancements
- Implement user authentication for organizers and attendees.
- Expand functionality to include notifications for upcoming events.
- Integrate analytics to track event success and attendee engagement.

## Contact
For questions or suggestions, feel free to reach out to me at:
- Email: hjamshaid@gmail.com
