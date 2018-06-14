FROM base-notebook:latest

LABEL maintainer="hxzhao <haoxiangzhao@outlook.com>"

RUN apk add python3-dev build-base linux-headers gcc freetype-dev libpng-dev &&\
    pip3 install numpy scipy matplotlib sympy &&\
    apk del python3-dev build-base linux-headers gcc freetype-dev libpng-dev &&\
    apk add libstdc++ libgcc freetype libpng