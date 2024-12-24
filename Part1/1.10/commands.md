# Exercise 1.10
https://devopswithdocker.com/part-1/section-5#exercise-110


## Commands:
``` bash
# Run the web server
docker run -d -p 8080:8080 web-server

# Test the server
curl http://localhost:8080
```