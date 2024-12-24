# Exercise 1.14
https://devopswithdocker.com/part-1/section-6#exercises-111-114

## Commands:
``` bash
# Build and run backend
docker build . -t example-backend && docker run -p 8080:8080 example-backend

# Build and run frontend
docker build . -t example-frontend && docker run -p 5000:5000 example-frontend
```