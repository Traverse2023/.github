# Motivation 👋

  There are several apps like Youtube, Discord, and Reddit, Marketplace where we are essentially communicating with millions of people. With Traverse, the idea is to combine these apps into one large social media platform. It's to learn approaches when developing huge apps like this and potentially use it ourselves with others when it is ready.


# Discord Clone Software Architecture Stack 👋

  Our Front End is built with React. The Back End currently consists of 2 microservices. The Main Service, is currently the first service the Front End contacts. It communicates with a Neo4j graph database. It handles users, their friendships, and their groups. For heavier storage, like the individual channels within the groups, and their messages are stored in a MongoDB noSQL database. Live messaging is done through the socket.io framework, which allows the usage of web sockets with lightweight code. There are plans to use AWS Websockets in the future instead of socket.io.

![Alt text](https://github.com/Traverse2023/.github/blob/d2893b42b710dc1502dfd6aa7d46c5a24e19a65e/profile/Traverse%20Architecture-2.png)

# Web App Link 👋

[Visit Traverse online!](http://traverse.us-east-1.elasticbeanstalk.com)

# Local Setup Instructions 👋

## Clone + Setup Repos
1. Create a directory named "Traverse" somewhere in your local machine.
2. cd into the directory.
3. git clone each repo.
4. For nodejs repos, use node version 16+/
5. Run npm install on nodejs projects.
6. Add .env file to traverse-ui
   - REACT_APP_BACKEND_URL=http://localhost:8000/
   - REACT_APP_STORAGE_SERVICE_URL=http://localhost:8080/

## Database Installation

### neo4j
1. Download neo4j desktop client: https://neo4j.com/deployment-center/#desktop
    - May have to scroll down to desktop section.
    - Install version 1.5.8
2. When you download, the website gives you a key that you will have to enter into the desktop client
3. In the client, create a new project called "Traverse"
4. In this project, create a new database called "Traverse"
5. You will be prompted to enter a password.
6. Start the DB and click "Open"
7. Create a .env file in the main-service directory.
   - NEO4J_URI=[URI listed from client]
   - NEO4J_USER=[User listed from client]
   - NEO4J_PASSWORD=[Password you set]
   - STORAGE_SERVICE_URL=http://localhost:8080
   - JWT_WEB_TOKEN=[token]
8. If set up correctly, you will be able to tun main_service (check additional steps for main_service in the repo)
  
### mongoDB
1. For storage-service, mvn install, and set java jdk, and run.
    - Using IntelliJ is recommended: https://www.jetbrains.com/idea/download/ 
2. Install mongoDB for your machine: https://www.mongodb.com/docs/manual/administration/install-community/
3. Install mongoDB compass: https://www.mongodb.com/try/download/compass
4. Start the DB on your machine
5. To verify, start main_service, traverse_ui, storage_service
    - Use traverse_ui to log in and go to Groups > Control Center > Create group
    - You should be able to create a group and chat, and the chat should update when you submit
