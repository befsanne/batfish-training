# What is this repository?

- This repository was created for my batfish training.
- Jupyter-notebook is written by Japanese.

# How to use

Detailed instructions are [here](batfish.md), but a short version is:
```
mkdir -p data
docker run -v $(pwd)/data:/data -p 9997:9997 -p 9996:9996 batfish/batfish
```

Then, run Jupyter-notebook as below:
```
cd notebooks
jupyter-notebook --no-browser
```

# License

- This software includes the work that is distributed in the Apache License 2.0.
