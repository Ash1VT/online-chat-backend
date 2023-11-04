# Online Chat Backend

This is the backend server for an Online Chat Application
built with Django and Django Channels. 
It was done in team as a project for University.


# Project Description

This backend server is the central component of an Online Chat Application built with Django, Django Channels, and Django Rest Framework. 
It serves as the core infrastructure for real-time messaging and collaboration, allowing users to connect, chat, and engage in conversations in a seamless and interactive manner.
The backend server is designed to work with the
corresponding [frontend client](https://github.com/Maksvell129/online-chat-frontend),
which is built with React and integrates with the server using the provided API.

### Technologies used:

1) **Django**: Django was selected as web framework due to its robustness, security features, and ease of development. 
It provides a solid foundation for building web applications and a powerful ORM system for managing data.
2) **Django Rest Framework**: For building the API endpoints and ensuring smooth communication between the frontend and backend, Django Rest Framework was integrated. 
This technology allows us to create a well-structured and user-friendly API that the React frontend can seamlessly interact with.
3) **Django Channels**: For real-time functionality, Django Channels were chosen to enable WebSocket support. 
This technology ensures that users can engage in live conversations with minimal latency, making it an ideal choice for a chat application.

### Challenges Faced: 

1) **Real-time Communication**: Implementing and managing real-time communication using WebSocket technology posed a significant challenge. 
It required careful planning to ensure that messages were delivered promptly and efficiently. 
2) **Security**: Maintaining the security of user data, messages, and authentication tokens was a top priority. 
Security measures were implemented, including authorization checks and encryption, to protect user privacy and data integrity. 

# Key Features:

1) **Real-time Messaging**: The **Online Chat Application** offers users the ability to send and receive messages in real-time.
Whether it's one-on-one conversations or group chats, users can engage in dynamic and immediate communication, making it an ideal platform for instant messaging.

2) **User Account Management**: Users can create their accounts by registering with their credentials. 
The registration process ensures that users have a unique identity on the platform, 
enabling them to customize their profiles and manage their chat history.

3) **User Authentication with JWT**: To secure the API endpoints and user data, the application employs **JWT (JSON Web Tokens)** authentication. 
When a user logs in, the backend generates a JWT token, which is then provided to the frontend. 
This token serves as a secure and efficient means of authenticating future requests, 
ensuring that only authorized users can access their accounts and messages.

4) **Django Channels for Real-time Communication**: To enable real-time communication between users, the **Online Chat Application** leverages **Django Channels**, 
a powerful Django library that extends the built-in ASGI (Asynchronous Server Gateway Interface) server with WebSocket support. 
This technology ensures that messages are delivered promptly and efficiently, allowing users to engage in live conversations with minimal latency.

# Local Development Environment

### Requirements

* Python 3.10 or higher
* pip
* virtualenv (optional)
* Redis
* PostgreSQL (if not using SQLite)

### Installation

1. Clone the repository to your local machine and navigate to the project directory.
    ```bash
    git clone https://github.com/Maksvell129/online-chat-backend
    cd online-chat-backend
    ```
2. Create a virtual environment and activate it (optional).
    ```bash
    virtualenv env
    source env/bin/activate
    ```
3. Install the project dependencies by running:
    ```bash
    pip install -r requirements.txt
    ```
4. Install Redis. You can download Redis from the official website or use your operating system's package manager to install it.
5. Create a `.env` file in the project root directory and add the following lines to it:
    ```
    USE_SQLITE=True
    REDIS_HOST=127.0.0.1
    ```
    This sets the database configuration to use SQLite by default and specifies the Redis server host to `127.0.0.1`.
    
    If you prefer to use PostgreSQL instead of SQLite update the database variables accordingly.
    ```
    DATABASE_NAME=mydatabase
    DATABASE_USER=myusername
    DATABASE_PASSWORD=mypassword
    DATABASE_HOST=localhost
    DATABASE_PORT=5432
    ```
6. Migrate the database by running:
    ```bash
    python manage.py migrate
    ```

### Running the Server

1. Start Redis server by running:
    ```bash
    redis-server
    ```
2. In a separate terminal window, start the Django development server by running:
    ```bash
    python manage.py runserver
    ```
3. Access the development server at `http://localhost:8000/`.

## Docker Compose

### Requirements

* Docker
* Docker Compose

### Installation

1. Clone the repository to your local machine and navigate to the project directory.
    ```bash
    git clone https://github.com/Maksvell129/online-chat-backend
    cd online-chat-backend
    ```

### Running the Server

1. Build and run the Docker containers by running the following command:
    ```bash
    docker-compose up --build
    ```

2. Access the development server at `http://localhost:8000/`.


### Actions

* Start the containers:
    ```bash
    docker-compose up
    ```
* Stop the containers:
    ```bash
    docker-compose down
    ```
* Create superuser
   ```bash
   docker-compose run web python manage.py createsuperuser
   ```

# Credits

Development team:
1) https://github.com/Ash1VT
2) https://github.com/Maksvell129
3) https://github.com/Egorfog