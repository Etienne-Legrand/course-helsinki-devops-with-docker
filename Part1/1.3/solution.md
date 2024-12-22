# Exercise 1.3
https://devopswithdocker.com/part-1/section-2#exercise-14

Secret message is: 'You can find the source code here: https://github.com/docker-hy'

## Commands:
``` bash
# Run the container in detached mode
docker run -d devopsdockeruh/simple-web-service:ubuntu

# Access the container using bash
docker exec -it 8d bash

# Follow the logs
root@8daf1f475f4b:/usr/src/app# tail -f ./text.log
```