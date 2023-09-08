# Motivation 👋

  There are several apps like Youtube, Discord, and Reddit, Marketplace where we are essentially communicating with millions of people. With Traverse, the idea is to combine these apps into one large social media platform. It's to learn approaches when developing huge apps like this and potentially use it ourselves with others when it is ready.


# Discord Clone Software Architecture Stack 👋

  Our Front End is built with React. The Back End currently consists of 2 microservices. The Main Service, is currently the first service the Front End contacts. It communicates with a Neo4j graph database. It handles users, their friendships, and their groups. For heavier storage, like the individual channels within the groups, and their messages are stored in a MongoDB noSQL database. Live messaging is done through the socket.io framework, which allows the usage of web sockets with lightweight code. There are plans to use AWS Websockets in the future instead of socket.io.

![Alt text](https://github.com/Traverse2023/.github/blob/0e9061f0748e21cc6ff09e9fb011fc5edd5b564f/profile/Traverse%20Architecture.png?raw=true)
