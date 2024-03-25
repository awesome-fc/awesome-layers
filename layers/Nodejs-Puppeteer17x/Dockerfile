FROM aliyunfc/runtime-nodejs14:build-latest

ENV PATH /opt/bin:$PATH
ENV LD_LIBRARY_PATH /opt/lib
ENV NODE_PATH /opt/nodejs/node_modules
WORKDIR /tmp

# install nodejs package
COPY ./package.json /opt/nodejs/
RUN cd /opt/nodejs \
    && npm --registry https://registry.npmmirror.com i

# install shared libraries
RUN mkdir -p /opt/lib /tmp/install
RUN apt-get update && apt-get install -y -d -o=dir::cache=/tmp/install \
    libblas3 fonts-liberation libappindicator3-1 libasound2 libatk-bridge2.0-0 \
    libgtk-3-0 libnspr4 libnss3 libpangocairo-1.0-0 libxcb-dri3-0 \
    libx11-xcb1 libxcb1 libxss1 libxtst6 lsb-release \
    xdg-utils libatspi2.0-0 libatk1.0-0 libxkbcommon0 libepoxy0 \
    libglapi-mesa libnspr4 libgbm-dev \
    --reinstall --no-install-recommends

RUN for f in $(ls /tmp/install/archives/*.deb); do \
        echo "Preparing to unpack ${f##*/}"; \
        cd /tmp/install/archives; \
        dpkg-deb -x ${f##*/} /tmp/install; \
    done;

# copy libraries to /opt/lib
RUN cp -r /tmp/install/usr/bin /opt/; \
    cp -r /tmp/install/usr/lib/x86_64-linux-gnu/* /opt/lib/

# zip file
# -y   store symbolic links as the link instead of the referenced file
# .[^.]*    including hidden files and exclude the parent directory
RUN cd /opt \
    && zip -ry layer.zip * .[^.]*

CMD ["bash"]
