FROM debian:jessie-backports
ENV POPPLER_VERSION 0.62.0
RUN apt-get update && apt-get install -t jessie-backports  \
    wget \
    build-essential \
    pkg-config \
    libfontconfig1-dev \
    cmake \
    libopenjpeg-dev \
    libjpeg-dev \
    libopenjp2-7-dev \
    libnss3-dev \
    libnss3-tools \
    unzip -y
RUN wget https://poppler.freedesktop.org/poppler-$POPPLER_VERSION.tar.xz
RUN tar -xf poppler-$POPPLER_VERSION.tar.xz \
    && cd poppler-$POPPLER_VERSION \
    && mkdir build && cd build && cmake .. -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=release \
    && make && make install \
    && mkdir $HOME/.mozilla/firefox -p \
    && mkdir /etc/pki/nssdb -p \
COPY pass .
RUN certutil -N -d sql:/etc/pki/nssdb -f pass
