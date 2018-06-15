# base-notebook

**The offical** is https://hub.docker.com/r/jupyter/base-notebook/. **Please be care**.

This image is equal to [jupyter/base-notebook](https://hub.docker.com/r/jupyter/base-notebook/), and only have base function of [Jupyter Notebook](https://github.com/jupyter/notebook).


## Get
You can get this by 
```
docker pull hxzhao527/docker-stacks-fake:base
```

## Use
First start one container from image
```
docker run --name base_notebook_web -p 12346:8888 -d hxzhao527/docker-stacks-fake:base
```
Use 
```
docker logs base_notebook_web
``` 
to get token for login notebook.

