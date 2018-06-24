FROM alpine:latest

LABEL maintainer="hxzhao <haoxiangzhao@outlook.com>"

RUN sed -i 's/http:\/\/dl-cdn.alpinelinux.org/https:\/\/mirrors.ustc.edu.cn/g' /etc/apk/repositories &&\
    apk add --no-cache tini python3 python3-dev build-base linux-headers &&\
    pip3 install notebook -i https://mirrors.ustc.edu.cn/pypi/web/simple &&\
    apk del --no-cache python3-dev build-base linux-headers &&\
    apk add --no-cache libstdc++ libgcc &&\
    mkdir -p /ext

ADD jupyter_notebook_config.py /root/.jupyter/jupyter_notebook_config.py

CMD ["/bin/sh", "-c", "jupyter notebook"]