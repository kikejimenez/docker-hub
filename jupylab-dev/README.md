# Docker-Jupyterlab-Dev

Dockerfile for Jupyterlab 3. It has the following custom  settings:

- yapf code formatter
- collapse headings
- xeus-python
- python-language-server
- python's nbdev

## Usage

Create an image by running on the root folder:

```bash
docker build -t jupylab-dev . 
```

## Docker Run Example

```bash
docker run --name ejr_container  -e NB_USER=enrique -e JUPYTER_ENABLE_LAB=yes -v $PWD:/wd -w /wd  -p 8881:8888 ejimenezr/jupylab-dev 
```

## Author

Enrique Jimenez
