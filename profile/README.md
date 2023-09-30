# Motivation 👋

  There are several apps like Youtube, Discord, and Reddit, Marketplace where we are essentially communicating with millions of people. With Traverse, the idea is to combine these apps into one large social media platform. It's to learn approaches when developing huge apps like this and potentially use it ourselves with others when it is ready.


# Discord Clone Software Architecture Stack 👋

  Our Front End is built with React. The Back End currently consists of 2 microservices. The Main Service, is currently the first service the Front End contacts. It communicates with a Neo4j graph database. It handles users, their friendships, and their groups. For heavier storage, like the individual channels within the groups, and their messages are stored in a MongoDB noSQL database. Live messaging is done through the socket.io framework, which allows the usage of web sockets with lightweight code. There are plans to use AWS Websockets in the future instead of socket.io.

![Alt text](https://github.com/Traverse2023/.github/blob/0e9061f0748e21cc6ff09e9fb011fc5edd5b564f/profile/Traverse%20Architecture-2.png?raw=true)


# Local Setup Instructions 👋

1. Create directory named "Traverse" in local machine.
2. Cd into the directory.
3. git clone each repo.
4. For nodejs repos, use node version 16+/
5. Run npm install on nodejs projects.
6. Download neo4j desktop client: https://neo4j.com/deployment-center/#desktop
    - May have to scroll down to desktop section.
    - Install version 1.5.8 
7. Create env file for main-service.
   - NEO4J_URI=...
   - NEO4J_USER=...
   - NEO4J_PASSWORD=...
8. For storage-service, mvn install, and set java jdk, and run.
