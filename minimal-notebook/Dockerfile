FROM hxzhao527/docker-stacks-fake:base

LABEL maintainer="hxzhao <haoxiangzhao@outlook.com>"

ADD minimal-notebook/_inside/ /ext/

RUN apk add git vim curl wget unzip xz fontconfig perl &&\
    cd /ext &&\
    wget https://github.com/jgm/pandoc/releases/download/2.2.1/pandoc-2.2.1-linux.tar.gz &&\
    tar xzf pandoc-2.2.1-linux.tar.gz &&\
    cp pandoc-2.2.1/bin/pandoc* /usr/bin/ &&\
    cd /ext &&\
    wget https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet/install-tl-unx.tar.gz &&\
    tar xzf install-tl-unx.tar.gz &&\
    cd install-tl-20180614/ &&\
    ./install-tl -profile /ext/texlive.profile &&\
    export PATH=$PATH:/usr/local/texlive/2018/bin/x86_64-linuxmusl/ &&\
    tlmgr install adjustbox collectbox ucs &&\
    cd / &&\
    rm -r /ext &&\
ENV PATH="$PATH:/usr/local/texlive/2018/bin/x86_64-linuxmusl/"
