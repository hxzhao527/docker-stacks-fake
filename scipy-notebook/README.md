# scipy-notebook

**The offical** is https://hub.docker.com/r/jupyter/scipy-notebook/. **Please be careful!!** 

This image is equal to [jupyter/scipy-notebook](https://hub.docker.com/r/jupyter/scipy-notebook/).


## Get
You can get this by 
```
docker pull hxzhao527/docker-stacks-fake:scipy
```

## Use
First start one container from image
```
docker run --name base_notebook_web -p 12346:8888 -d hxzhao527/docker-stacks-fake:scipy
```
Use 
```
docker logs base_notebook_web
``` 
to get token for login notebook.