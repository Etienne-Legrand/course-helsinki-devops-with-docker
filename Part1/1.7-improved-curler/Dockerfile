FROM ubuntu:22.04

# Install curl
RUN apt-get update && apt-get install -y curl

# Run the script
WORKDIR /usr/src/app
COPY  script.sh .
ENTRYPOINT ["./script.sh"]
