# Airbnb Clone Project

## Description
This project is part of the ALX Backend Development program.  
The goal is to build a simple clone of the Airbnb platform to learn about backend development, databases, APIs, and deployment.

## Learning Objectives
- Understand how to structure and manage a project repository with Git and GitHub.
- Collaborate effectively with team members using version control.
- Learn the basics of backend architecture and database design.
- Document and plan project features and workflows.

## Technology Stack

- **Django**: A web framework for building RESTful APIs and handling server-side logic.  
- **PostgreSQL**: A relational database used to store and manage application data securely.  
- **GraphQL**: A query language for APIs that allows clients to request exactly the data they need.  
- **Docker**: Containerization tool to package the application and its dependencies for easy deployment.  
- **Git & GitHub**: Version control system and repository hosting service for tracking changes and collaboration.

## Database Design

### Entities and Fields

- **Users**  
  - id (primary key)  
  - name  
  - email  
  - password  
  - role  
  *Relationships:* A user can have multiple properties and multiple bookings.  

- **Properties**  
  - id (primary key)  
  - title  
  - description  
  - location  
  - owner_id (foreign key to Users)  
  *Relationships:* Each property belongs to a user (owner) and can have multiple bookings and reviews.  

- **Bookings**  
  - id (primary key)  
  - property_id (foreign key to Properties)  
  - user_id (foreign key to Users)  
  - start_date  
  - end_date  
  *Relationships:* A booking belongs to one property and one user.  

- **Reviews**  
  - id (primary key)  
  - property_id (foreign key to Properties)  
  - user_id (foreign key to Users)  
  - rating  
  - comment  
  *Relationships:* A review belongs to a property and a user.  

- **Payments**  
  - id (primary key)  
  - booking_id (foreign key to Bookings)  
  - amount  
  - payment_date  
  - status  
  *Relationships:* Each payment is linked to one booking.

## Feature Breakdown

- **User Management**  
  Allows users to create accounts, log in, and manage their profile information. This ensures that only registered users can book properties or leave reviews.  

- **Property Management**  
  Enables property owners to add, update, and delete their listings. Users can browse available properties with detailed descriptions and images.  

- **Booking System**  
  Lets users book available properties for specific dates. It tracks availability, prevents double bookings, and links bookings to users and properties.  

- **Review System**  
  Allows users to leave ratings and comments for properties they have stayed at. This helps maintain quality and provides feedback for property owners.  

- **Payment Processing**  
  Handles payments for bookings securely, recording payment status and linking transactions to bookings. This ensures smooth and reliable financial transactions.


## API Security

- **Authentication**  
  Ensures that only registered users can access protected endpoints by verifying their identity. This protects user accounts and sensitive data.  

- **Authorization**  
  Controls what actions each user can perform based on their role (e.g., user vs. property owner). This prevents unauthorized access to restricted resources.  

- **Rate Limiting**  
  Limits the number of requests a user can make in a given time. This helps prevent abuse and protects the server from being overloaded.  

- **Data Encryption**  
  Encrypts sensitive data, such as passwords and payment information, both in transit and at rest. This ensures user privacy and secures financial transactions.  

- **Input Validation & Sanitization**  
  Validates and cleans incoming data to prevent security vulnerabilities like SQL injection or XSS attacks. This keeps the application and its users safe.


## Team Roles

- **Backend Developer**: Responsible for building and maintaining the server-side logic, APIs, and ensuring that the application works smoothly with the database and frontend.

- **Database Administrator (DBA)**: Manages the database, ensures data integrity, optimizes queries, and handles backups and security.

- **Frontend Developer**: Implements the user interface and user experience, making sure the app looks good and is easy to use.

- **Project Manager**: Oversees the project, coordinates the team, sets deadlines, and ensures that the project stays on track.

- **QA Engineer / Tester**: Tests the application to find bugs, ensures the functionality works as expected, and maintains quality standards.

## Author
- **ILYAS EL ATTAR**
