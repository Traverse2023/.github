# Motivation 👋

  There are several apps like Youtube, Discord, and Reddit, Marketplace where we are essentially communicating with millions of people. With Traverse, the idea is to combine these apps into one large social media platform. It's to learn approaches when developing huge apps like this and potentially use it ourselves with others when it is ready.


# Discord Clone Software Architecture Stack 👋

  Our Front End is built with React. The Back End currently consists of 2 microservices. The Main Service, is currently the first service the Front End contacts. It communicates with a Neo4j graph database. It handles users, their friendships, and their groups. For heavier storage, like the individual channels within the groups, and their messages are stored in a MongoDB noSQL database. Live messaging is done through the socket.io framework, which allows the usage of web sockets with lightweight code. 

![Alt text](https://github.com/Traverse2023/.github/blob/5aef5e77b4eba183a548cbafb7114ef61c568d7a/profile/Traverse%20Architecture-3.png)

# Local Setup Instructions 👋


### For a containerized local deployment:

1. [Download docker](https://www.docker.com/products/docker-desktop/)
   
2. Cd into a directory where you would want the Traverse project

3. Clone Traverse root repo and enter Traverse directory

  ```
  git clone --recursive https://github.com/Traverse2023/Traverse.git && cd Traverse
  ```

4. Run to pull current main branches for submodules
   
  ```
  git submodule foreach git pull origin main && git submodule foreach git checkout main
  ```

 
5. Run all containers locally using docker
   
  ```
  docker compose up
  ```
   For hot reload/restart enabled:

  ```
  docker compose watch
  ```

  
