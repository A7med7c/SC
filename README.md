useCaseDiagram
    actor "Customer" as C
    actor "Admin" as A
    
    package "Event Planning System" {
        %% Account Management
        usecase "Register & Log In" as UC1
        usecase "Manage Profile" as UC2
        
        %% Event Planning & Booking
        usecase "Select Event Category" as UC3
        usecase "Search & Select Venue" as UC4
        usecase "Customize Budget & Package" as UC5
        usecase "Book Event" as UC6
        usecase "Make Payment" as UC7
        usecase "Modify Booking" as UC8
        usecase "Track Booking Status" as UC9
        
        %% Social & Communication
        usecase "Invite Guests" as UC10
        usecase "Rate Venue / Add to Favorites" as UC11
        usecase "Submit Complaint / Feedback" as UC12
        usecase "Request Offline Meeting" as UC13
        usecase "Chat with Bot / Support" as UC14
        
        %% Admin Functions
        usecase "Manage Venues" as UC15
        usecase "Manage Packages & Budgets" as UC16
        usecase "Manage Bookings" as UC17
        usecase "Track Payments" as UC18
        usecase "Respond to Complaints" as UC19
    }

    %% Customer Relationships
    C --> UC1
    C --> UC2
    C --> UC3
    C --> UC4
    C --> UC5
    C --> UC6
    C --> UC7
    C --> UC8
    C --> UC9
    C --> UC10
    C --> UC11
    C --> UC12
    C --> UC13
    C --> UC14

    %% Admin Relationships
    A --> UC1
    A --> UC15
    A --> UC16
    A --> UC17
    A --> UC18
    A --> UC19
    A --> UC13
    
    %% Relationships between Use Cases (Includes/Extends)
    UC6 ..> UC7 : <<include>>
    UC4 ..> UC3 : <<include>>
    UC15 ..> UC1 : <<include>>
