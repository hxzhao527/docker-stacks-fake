# mini-notebook

**The offical** is https://hub.docker.com/r/jupyter/minimal-notebook/. **Please be care**.

This image is equal to [jupyter/minimal-notebook](https://hub.docker.com/r/jupyter/minimal-notebook/), except editor. There is only vim here.(Maybe it is not necessary too.)

## Comment:
As you see, this image size is increasing rapidly. [texlive](https://www.tug.org/texlive/) is too large, but if you want to convert .ipynb to other format like pdf, it seems to be necessary.

In my opinion, ```Save as PDF``` is not necessary. If you want to share your code, ```ipnb``` is enough, or save image draw in notebook, just right-click to save. 

So if you don't need this, just change ```Dockerfile```.