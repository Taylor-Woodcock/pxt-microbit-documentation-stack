# pxt-microbit-documentation-stack
A Docker-compose stack built to assist in the editing of pxt-microbit documentation markdown files. This stack includes a pxt-microbit instance and a code-server web-based VSCode instance, tied together to allow online editing of the .MD files.

## Local Server
### Running

```
git clone https://github.com/Taylor-Woodcock/pxt-microbit-documentation-stack --recurse-submodules
cd pxt-microbit-documentation-stack
git submodule update --init --recursive --remote
chmod -R a+rwx energyinschools-pxt-documentation/
docker-compose -f "docker-compose.yml" up -d --build
```

Coder will be hosted on port `8443`, while the pxt-microbit instance will be hosted on port `8080`.
To access Coder, visit `localhost:8443`. To access the block editor, visit `localhost:8080`.

### Editing Documents
To edit the pxt-microbit documentation files, first naviage to `localhost:8443` in your browser. This will launch an online version of Visual Studio Code, which has its volume mapped to the `/docs` folder in this repository.

**Note: The default password for this project is `testing`.**

In another tab, browse to `localhost:8080/docs` and navigate to the desired documentation file you wish to edit. With this live view open, go back to the VSCode tab and locate the same file within the project view to the left. The files will be located at the same location within the URL (e.g. `localhost:8080/about` will be `/about.md`. `localhost:8080/projects/test` will be `/projects/test.md`).

With the markdown (MD) file open in VSCode, and with the live site open in another tab, you can now start to make live changes to the documents. A nice way to quickly preview the markdown file is to open a split preview in VSCode. To do this, locate the button at the top right of the editor that has a blue magnifying glass.

One changes are made to the markdown files, save the file and navigate back to the Block Editor tab with the documentation file open. Refresh this page and you will now see the updated view of the file.

**Tip: Enabling autosave can help make quick changes!**

### Updating EiS

The `/docs` folder has been moved to [its own submodule](https://github.com/Taylor-Woodcock/energyinschools-pxt-documentation). This repo can be updated and will hold all changes made to the documents using this system.

## Project Notes
This project was made as a learning process for Docker and Docker-Compose. I have produced a [DockerHub repository](https://hub.docker.com/r/twoodcock/pxt-microbit) of the [pxt-microbit](https://github.com/microsoft/pxt-microbit) that can be pulled and run independently from this stack.

```
docker pull twoodcock/pxt-microbit
```
