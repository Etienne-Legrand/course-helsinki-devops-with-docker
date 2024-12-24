# Exercise 1.9
https://devopswithdocker.com/part-1/section-5#exercise-19

## Commands:
``` bash
# Create an empty log file locally to avoid Docker creating a directory instead
touch text.log

# Run the container and mount the local log file to capture logs from the container
docker run -v "$(pwd)/text.log:/usr/src/app/text.log" devopsdockeruh/simple-web-service:alpine
```