# What is this repository?

- This repository was created for my batfish training.

# How to run

Detailed instructions are [here](batfish.md), but a short version is:
```
mkdir -p data
docker run -v $(pwd)/data:/data -p 9997:9997 -p 9996:9996 batfish/batfish
```

# License

- This software includes the work that is distributed in the Apache License 2.0.

# Original README

- See below:

---

**Got questions, feedback, or feature requests? Join our community on [Slack!](https://join.slack.com/t/batfish-org/shared_invite/enQtMzA0Nzg2OTAzNzQ1LTUxOTJlY2YyNTVlNGQ3MTJkOTIwZTU2YjY3YzRjZWFiYzE4ODE5ODZiNjA4NGI5NTJhZmU2ZTllOTMwZDhjMzA)**

# Batfish Docker Containers

This repo has the source files to build `Batfish` and `allinone` docker containers that provide a quick way to start using Batfish. The `Batfish` container has only the core [Batfish](https://github.com/batfish/batfish) service, and the `allinone` container also inlcudes [Pybatfish](https://github.com/batfish/pybatfish). 

We recommend using the `Batfish` container if you plan to analyze your own network data, and the `allinone` container if you want to just play with the example data and Jupyter notebooks bundled with Pybatfish. 

## Running the `Batfish` container

Detailed instructions are [here](batfish.md), but a short version is:
```
mkdir -p data
docker run -v $(pwd)/data:/data -p 9997:9997 -p 9996:9996 batfish/batfish
```
These commands start the service, and you can then use [Pybatfish](https://github.com/batfish/pybatfish) to interact with it.

## Running the `allinone` container

Detailed instructions are [here](allinone.md), but a short version is:
```
docker run -p 8888:8888 batfish/allinone
```
When this container starts, Jupyter will show a token required for access (e.g. token=abcdef123456...). Navigate to http://localhost:8888 in a web browser on the host machine and enter this token in the "Password or token:" prompt to access the notebooks.

## Building and pushing containers

If you are a developer of Batfish, see [dev instructions](README.dev.md) on how to build images and push them to Docker Hub.
