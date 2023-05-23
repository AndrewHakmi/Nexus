This page wil guide you through the installation and setup for docker.

Step 1: 
Install Docker

Step 2:
Pull the latest image from docker 
`:::shell
 docker pull significantgravitas/auto-gpt`

Step 3:
Create a folder for Auto-GPT inside the container??

Step 4:
In the folder create a new file and name it "docker-compose.yml"

Step 5:
Open the file you just created and copy the following code to it

`:::yaml
 version: "3.9"
 services:
   auto-gpt:
     image: significantgravitas/auto-gpt
     depends_on:
       - redis
     env_file:
       - .env
     environment:
       MEMORY_BACKEND: ${MEMORY_BACKEND:-redis}
       REDIS_HOST: ${REDIS_HOST:-redis}
     profiles: ["exclude-from-up"]
     volumes:
       - ./auto_gpt_workspace:/app/autogpt/auto_gpt_workspace
       - ./data:/app/data
       ## allow auto-gpt to write logs to disk
       - ./logs:/app/logs
       ## uncomment following lines if you want to make use of these files
       ## you must have them existing in the same folder as this docker-compose.yml
       #- type: bind
       #  source: ./azure.yaml
       #  target: /app/azure.yaml
       #- type: bind
       #  source: ./ai_settings.yaml
       #  target: /app/ai_settings.yaml
   redis:
     image: "redis/redis-stack-server:latest"`

This concludes installing with Docker. Continue your journey on the "Configuring Auto-GPT" page