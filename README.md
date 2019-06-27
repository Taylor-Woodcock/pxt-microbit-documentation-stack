# pxt-microbit-documentation-stack
A Docker-compose stack built to assist in the editing of pxt-microbit documentation markdown files. This stack includes a pxt-microbit instance and a code-server web-based VSCode instance, tied together to allow online editing of the .MD files.

## Local Server
### Running

```
git clone https://github.com/Taylor-Woodcock/pxt-microbit-documentation-stack
cd pxt-microbit-documentation-stack
docker-compose -f "docker-compose.yml" up -d --build
```

Coder will be hosted on port `8443`, while the pxt-microbit instance will be hosted on port `8080`.

### Node Modules (DAPjs)
At the moment, this repo has not been cleaned up and may contain a load of potentially useless (for this project) node modules.
That being said, this project relies on the [DAPjs](https://github.com/ARMmbed/dapjs) JavaScript interface for the main serial communication between the webapp and the bridging micro:bit.
To install the required node modules, be sure to run ``npm install`` before running the server.

## Project Notes
This project was made as a learning process for Docker and Docker-Compose. I have produced a [DockerHub repository](https://hub.docker.com/r/twoodcock/pxt-microbit) of the [pxt-microbit](https://github.com/microsoft/pxt-microbit) that can be pulled and run independently from this stack.

```
docker pull twoodcock/pxt-microbit
```
