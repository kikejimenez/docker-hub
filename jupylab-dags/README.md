# Docker-Jupylab-dags

> Requires .ssh git credentials

## Usage

Create an image by running on the root folder:

```bash
docker build -t jupylab-dags . 
```

Tag a version:

```bash
docker tag ejimenezr/jupylab-dags:lates
```

Push to docker-hub:

```bash
docker push ejimenezr/jupylab-dags:latest
```

## Docker Run Example

```bash
docker run --rm -it -v ~/.ssh:/home/jovyan/.ssh  jupylab-dags bash/home/jovyan 
```

## Author

Enrique Jimenez
