FROM ubuntu:18.04
LABEL maintainer="support@globalmaksimum.com"

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8

RUN apt-get update && apt-get install -y \
wget && \
#libgit2-dev && \
#zlib1g-dev && \
rm -rf /var/lib/apt/lists/*

RUN wget https://mirrors.kernel.org/ubuntu/pool/main/libp/libpng/libpng12-0_1.2.54-1ubuntu1_amd64.deb && \
dpkg -i libpng12-0_1.2.54-1ubuntu1_amd64.deb && \
rm libpng12-0_1.2.54-1ubuntu1_amd64.deb

RUN wget https://mran.blob.core.windows.net/install/mro/3.5.1/microsoft-r-open-3.5.1.tar.gz && \
tar -xzvf microsoft-r-open-3.5.1.tar.gz && \
cd microsoft-r-open  && \
./install.sh -a -u && \
cd .. && \
rm -rf microsoft-r-open && \
rm microsoft-r-open-3.5.1.tar.gz

CMD ["R"]