FROM hxzhao527/docker-stacks-fake:base

LABEL maintainer="hxzhao <haoxiangzhao@outlook.com>"

RUN apk add python3-dev build-base linux-headers gfortran gcc freetype-dev libpng-dev lapack-dev &&\
    pip3 install --upgrade pip -i https://mirrors.ustc.edu.cn/pypi/web/simple &&\
    pip3 install numpy scipy matplotlib sympy pandas seaborn openpyxl plotly -i https://mirrors.ustc.edu.cn/pypi/web/simple &&\
    apk del python3-dev build-base linux-headers gfortran gcc freetype-dev libpng-dev &&\
    apk add libstdc++ libgcc freetype libpng lapack