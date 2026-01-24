```mermaid
usecaseDiagram
    actor "Guest" as G
    actor "Registered User" as U
    actor "Event Planner" as P
    actor "Administrator" as A

    package "Event Planning System" {
        usecase "Register" as UC1
        usecase "Login" as UC2
        usecase "Search for Events" as UC3
        usecase "View Event Details" as UC4
        usecase "Book Ticket / Reserve" as UC5
        usecase "Make Payment" as UC6
        usecase "Cancel Reservation" as UC7
        usecase "Create New Event" as UC8
        usecase "Update/Delete Event" as UC9
        usecase "View Booking Status" as UC10
        usecase "Manage Users" as UC11
        usecase "Generate Reports" as UC12
        usecase "Provide Feedback" as UC13
    }

    %% Guest Relationships
    G --> UC1
    G --> UC3
    G --> UC4

    %% User Relationships
    U --> UC2
    U --> UC3
    U --> UC4
    U --> UC5
    U --> UC7
    U --> UC13

    %% Event Planner Relationships
    P --> UC2
    P --> UC8
    P --> UC9
    P --> UC10

    %% Administrator Relationships
    A --> UC2
    A --> UC11
    A --> UC12

    %% Includes and Extends
    UC5 ..> UC6 : <<include>>
    UC5 ..> UC2 : <<include>>
    UC8 ..> UC2 : <<include>>
```
