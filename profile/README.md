# Motivation 👋

  We want to make a platform where users can solve algorithmic coding problems together in a multiplayer fashion. The first phase of the project would start off with the communication platform, which we are internally calling CodeChat or HackerTalk. HackerTalk will allow users to message, voice, video chat, send snippets of code, share screen, and other functionalities.
The second phase is the actual coding platform called DevDuel. DevDuel would allow users to compete against each other with algorithmic-style progamming questions.

The most common use case would be to create an account, add friends, create a group, then start a DevDuel with your friends. Based on who finishes first/has most efficient solution, there will be a leaderboard at the end of the session. 

We also want to expand to other use cases. If you are a CS student, this has to be the place to be to talk, live, and breath code.


# HackerTalk Software Architecture Stack 👋

![Alt text](https://github.com/Traverse2023/.github/blob/2fdfe67e887555c7bfd894cb823c14d809da2f98/profile/Traverse%20Architecture-5.png)

# Deployment Process

![Alt text](https://github.com/Traverse2023/.github/blob/8a81df02b2cc5e4c2ef0f43aea2b949547c14ec8/profile/CICD.png)

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

  
