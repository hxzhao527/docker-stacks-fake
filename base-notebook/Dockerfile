FROM alpine:latest

LABEL maintainer="hxzhao <haoxiangzhao@outlook.com>"

ENV port 8888

RUN sed -i 's/http:\/\/dl-cdn.alpinelinux.org/https:\/\/mirrors.ustc.edu.cn/g' /etc/apk/repositories &&\
    apk update &&\
    apk add python3 python3-dev build-base linux-headers &&\
    pip3 install notebook -i https://mirrors.ustc.edu.cn/pypi/web/simple &&\
    apk del python3-dev build-base linux-headers &&\
    apk add libstdc++ libgcc

EXPOSE ${port}

CMD ["/bin/sh", "-c", "jupyter notebook --no-browser --allow-root --ip 0.0.0.0 --port ${port}"]