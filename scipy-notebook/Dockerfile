FROM hxzhao527/docker-stacks-fake:minimal

LABEL maintainer="hxzhao <haoxiangzhao@outlook.com>"

RUN apk add --no-cache python3-dev build-base linux-headers gfortran gcc freetype-dev libpng-dev lapack-dev &&\
    pip3 install numpy scipy matplotlib pandas openpyxl XlsxWriter plotly -i https://mirrors.ustc.edu.cn/pypi/web/simple &&\
    apk del --no-cache python3-dev build-base linux-headers gfortran gcc freetype-dev libpng-dev &&\
    apk add --no-cache libstdc++ libgcc freetype libpng lapack