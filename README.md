# Docker-conda-dash-nginx-gunicorn

This project contains a dockerized Hello-world-type 'Hello Dash' Dash application running in a Conda environment to use as a template for your own project. Gunicorn is used for serving and Nginx for reverse proxy. The Dash application image and the Nginx image are built together using docker-compose.

## File structure

- build.sh
- dash_app
    - app.py
    - Dockerfile
    - environment.yml
    - __init__.py
- docker-compose.yml
- nginx
    - Dockerfile
    - nginx.conf
    - project.conf
- README.md

## Getting started

1. Install docker and docker-compose
2. Run the build script

```bash
sudo bash build.sh
```

3. Start the container with docker-compose from the project root

```bash
sudo docker-compose up
```

4. Verify that the "Hello Dash" application is visible at localhost:80
5. Start coding your own dash application. The cleanest way to modify the python environment is to change the package list in dash_app/environment.yml and rebuild the docker image.
