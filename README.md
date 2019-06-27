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
To access Coder, visit `localhost:8443`. To access the block editor, visit `localhost:8080`.

## Project Notes
This project was made as a learning process for Docker and Docker-Compose. I have produced a [DockerHub repository](https://hub.docker.com/r/twoodcock/pxt-microbit) of the [pxt-microbit](https://github.com/microsoft/pxt-microbit) that can be pulled and run independently from this stack.

```
docker pull twoodcock/pxt-microbit
```
