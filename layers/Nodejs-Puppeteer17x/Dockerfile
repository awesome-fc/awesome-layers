FROM aliyunfc/runtime-nodejs14:build-latest

ENV PATH /var/fc/lang/nodejs14/bin:/opt/bin:$PATH
ENV LD_LIBRARY_PATH /opt/lib
ENV NODE_PATH /opt/nodejs/node_modules

WORKDIR /tmp

COPY ./package.json /opt/nodejs/
RUN cd /opt/nodejs \
    && npm --registry https://registry.npm.taobao.org i

RUN mkdir -p /opt/lib && mkdir -p /tmp/install
RUN apt-get update
RUN apt-get install -y -d -o=dir::cache=/tmp/install \
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

RUN cp -r /tmp/install/usr/bin /opt/; \
    cp -r /tmp/install/usr/lib/x86_64-linux-gnu/* /opt/lib/

RUN cd /opt \
    && zip -ry layer.zip * .[^.]*

CMD ["bash"]