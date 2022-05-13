# Docker Jupylab-dev and github CLI

Dockerfile for Jupyterlab 3. It has the following custom  settings:

- uses jupylab-dev image 
- installs github CLI

## Usage

Create an image by running on the root folder:

```bash
docker build -t jupylab-gh . 
```

Tag a version:

```bash
docker tag jupylab-gh  ejimenezr/jupylab-gh:latest
```

Push to docker-hub:

```bash
docker push ejimenezr/jupylab-gh:latest
```

## Docker Run Example

```bash
docker run --name ejr_container  -e NB_USER=enrique -e JUPYTER_ENABLE_LAB=yes -v $PWD:/wd -w /wd  -p 8881:8888 ejimenezr/jupylab-gh 
```

## Author

Enrique Jimenez
