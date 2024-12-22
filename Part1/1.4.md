# Exercise 1.4
https://devopswithdocker.com/part-1/section-2#exercise-14

## Commands solution 1:

```bash
# Run an Ubuntu container and execute a loop to read and curl a website (need to exit because curl not found)
docker run ubuntu sh -c "while true; do echo 'Input website:'; read website; echo 'Searching..'; sleep 1; curl http://$website; done"

# Update package lists in the running container
docker exec -it 5 apt update

# Install curl in the running container
docker exec -it 5 apt install curl

# Execute a loop in the running container to read and curl a website
docker exec -it 5 sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
```

## Alternative solution 2:

```bash
# Run an Ubuntu container interactively
docker run -it ubuntu bash

# In the container install curl
apt update && apt install curl

# In the container execute a loop to read and curl a website
while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done
```

## Alternative solution 3 in one line:

```bash
# Run an Ubuntu container, update package lists, install curl, and execute a loop to read and curl a website
docker run -it ubuntu bash -c 'apt update && apt install -y curl && while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
```