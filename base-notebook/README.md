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
docker run --name base_notebook_web -p 12346:8888 -d --init hxzhao527/docker-stacks-fake:base
```
The default password is ```hxzhao527```, you can use env to reset it, like
```
docker run --name base_notebook_web -p 12346:8888 -d --init -e PASSWORD=ilovepython hxzhao527/docker-stacks-fake:base
```
