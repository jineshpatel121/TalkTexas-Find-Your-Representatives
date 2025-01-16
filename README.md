# TalkTexas: A Full-Stack Application to Contact Texas Representatives

## Overview
TalkTexas is a full-stack web application that displays information about Texas representatives. Users can view details such as representatives' names, titles, parties, districts, email addresses, phone numbers, and images. The app allows filtering representatives by district and is built with a React frontend, a Spring Boot backend, and a MySQL database.

## Features
- Display a list of Texas representatives with their details.
- Filter representatives by district.
- Responsive design with a clean UI.
- Fetch real-time data from the [Open States API](https://v3.openstates.org/people).
- Store representative data in a MySQL database.

## Project Structure
```plaintext
TalkTexas
├── talk_texas_front (React frontend)
│   ├── src
│   │   ├── components
│   │   │   └── RepresentativesList.js
│   │   ├── App.js
│   │   └── index.js
│   ├── public
│   └── package.json
├── texasAPI (Spring Boot backend)
│   ├── src
│   │   ├── main
│   │   │   ├── java
│   │   │   │   └── com.TalkTexas.texasAPi
│   │   │   │       ├── controller
│   │   │   │       │   └── PeopleController.java
│   │   │   │       ├── model
│   │   │   │       │   ├── Person.java
│   │   │   │       │   └── PersonDTO.java
│   │   │   │       ├── repository
│   │   │   │       │   └── PersonRepository.java
│   │   │   │       └── service
│   │   │   │           └── PeopleService.java
│   ├── pom.xml
├── README.md
└── database.sql (Database schema and initial setup)
```

## Technologies Used
### Frontend
- **React**: Used for building the user interface.
- **CSS**: For styling the components.

### Backend
- **Spring Boot**: Handles API requests, data processing, and database interaction.
- **MySQL**: Stores representative data.

### API
- **Open States API**: Provides representative data for Texas.

## Installation and Setup
### Prerequisites
1. **Node.js**: Ensure Node.js and npm are installed.
2. **Java**: Install Java Development Kit (JDK) 17 or higher.
3. **MySQL**: Install MySQL server.

### Backend Setup
1. Navigate to the `texasAPI` directory:
   ```bash
   cd TalkTexas/texasAPI
   ```
2. Configure the `application.properties` file to connect to your MySQL database:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/talktexas
   spring.datasource.username=<your-username>
   spring.datasource.password=<your-password>
   spring.jpa.hibernate.ddl-auto=update
   ```
3. Build and run the Spring Boot application:
   ```bash
   mvn spring-boot:run
   ```

### Frontend Setup
1. Navigate to the `talk_texas_front` directory:
   ```bash
   cd TalkTexas/talk_texas_front
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the React development server:
   ```bash
   npm start
   ```
4. Access the application in your browser at `http://localhost:3000`.

## Usage
1. Launch the backend and frontend servers as described in the setup instructions.
2. The homepage will display a list of representatives.
3. Use the dropdown to filter representatives by district.
4. Click on email addresses to send an email or contact them using their phone numbers.
5. Click on "More Info" tab for further details like office addresses and past legislative action


<img width="1470" alt="image" src="https://github.com/user-attachments/assets/e1d408a9-f249-4d9f-9684-73f6920bcb34" />
<img width="1470" alt="image" src="https://github.com/user-attachments/assets/11cb3c2a-d94e-4823-bd29-c71168ad9a6d" />


