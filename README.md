# Spring-boot-react-chat-web-app
This is a real-time chat application built using Spring Boot for the back-end and React.js for the front-end. The app supports user authentication, public chatrooms, private messaging, and allows users to search and add other users by their username. It is designed for ease of use, scalability, and a seamless messaging experience.

Features
User Authentication: Register, log in, and log out securely.
Public Chatroom: Engage with all users in a public space.
Private Messaging: Send direct messages to specific users.
User Search and Add: Search for users by their username and add them to your contact list.
Real-Time Communication: Instant message delivery with WebSockets.
Responsive Design: Optimized for both desktop and mobile devices.
Message History: View past messages in chatrooms.
User-Friendly Interface: Clean, intuitive UI for easy navigation.

Tech Stack
Front-end
React.js: For building user interfaces.
SockJS: WebSocket client for real-time communication.
STOMP: Protocol for WebSocket messaging.
React Router: For client-side routing.
Axios: For HTTP requests.
Tailwind CSS: For styling.
Back-end
Spring Boot: Java framework for web applications.
Spring WebSocket: WebSocket support in Spring.
Spring Data JPA: For database interactions.
MySQL: Relational database for storing user data.
Lombok: For reducing boilerplate code in Java.
Others
Maven: Build and dependency management tool.
Postman: For API testing and development.
How to Use
Register: Create a new account with a unique username and email.
Login: Enter your credentials to access the application.
Public Chat: Join the public chatroom to engage in group conversations.
Private Messaging: Click on a user's name to initiate a private chat.
Search Users: Use the search feature to find other users by their username and add them to your contacts.
Setup Instructions
Prerequisites
Ensure the following are installed on your system:

Node.js: Download Node.js
Java JDK: Download JDK
Maven: Download Maven
MySQL: Download MySQL
Front-end Setup
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/chat-application.git
cd chat-application/frontend
Install dependencies:

bash
Copy code
npm install
Start the React development server:

bash
Copy code
npm start
The app will be running at http://localhost:5173.

Back-end Setup
Navigate to the back-end directory:

bash
Copy code
cd ../backend
Configure MySQL database:

Create a MySQL database named chat.
Open src/main/resources/application.properties and update the database configurations:
properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/chat
spring.datasource.username=your_mysql_username
spring.datasource.password=your_mysql_password
Build and run the Spring Boot application:

bash
Copy code
mvn spring-boot:run
The back-end server will be running at http://localhost:8080.

WebSocket Configuration
Ensure the WebSocket connection is set up correctly in your React front-end (App.js or relevant file):

javascript
Copy code
const socket = new SockJS('http://localhost:8080/ws');
const stompClient = Stomp.over(socket);
Integrating Front-end and Back-end
Verify the front-end and back-end are communicating correctly:

Front-end: Running at http://localhost:5173.
Back-end: Running at http://localhost:8080.
API Endpoints
User Authentication
POST /api/users/signup: Register a new user.
POST /api/users/login: Log in an existing user.
Messaging
POST /app/message: Send a message to the public chatroom.
POST /app/private-message: Send a private message to a specific user.
User Operations
GET /api/users/search: Search for a user by username.
POST /api/users/add: Add a user to your contacts by their username.
Screenshots
Home Page (Login)

Registration Page

Public Chat Room

Private Chat

User Search

Note: Ensure the screenshots are placed in a screenshots directory at the root of your project.

Future Features
Video and Voice Calls: Implement real-time video and voice calls.
Message Reactions: Add the ability to react to messages with emojis.
Read Receipts: Show whether messages have been read by the recipient.
Message History: Save and retrieve chat history from the database.
Profile Customization: Allow users to upload profile pictures and customize their profile.
Typing Indicators: Display indicators when users are typing.
Status Indicators: Show online/offline status of users.
Push Notifications: Notify users of new messages or events.
Contributing
We welcome contributions! Please fork the repository and create a pull request with your feature or bug fix.

License
This project is licensed under the MIT License - see the LICENSE file for details.
