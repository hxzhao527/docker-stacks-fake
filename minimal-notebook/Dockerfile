FROM hxzhao527/docker-stacks-fake:base

LABEL maintainer="hxzhao <haoxiangzhao@outlook.com>"

ADD _inside/ /ext/

RUN apk add git vim curl wget unzip xz fontconfig perl &&\
    cd /ext &&\
    wget https://github.com/jgm/pandoc/releases/download/2.2.1/pandoc-2.2.1-linux.tar.gz &&\
    tar xzf pandoc-2.2.1-linux.tar.gz &&\
    cp pandoc-2.2.1/bin/pandoc* /usr/bin/ &&\
    cd /ext &&\
    tar xzf install-tl-unx.tar.gz &&\
    install-tl-20*/install-tl -profile /ext/texlive.profile &&\
    export PATH=$PATH:/usr/local/texlive/2018/bin/x86_64-linuxmusl/ &&\
    tlmgr install adjustbox collectbox ucs enumitem collection-fontsrecommended &&\
    cd / &&\
    rm -r /ext
ENV PATH="$PATH:/usr/local/texlive/2018/bin/x86_64-linuxmusl/"
