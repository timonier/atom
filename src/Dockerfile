FROM ubuntu:14.04
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    ATOM_VERSION=1.4.3 \
    DEBIAN_FRONTEND=noninteractive \
    NO_AT_BRIDGE=1

RUN set -x \

    # Prepare system

    && apt-get update \

    # Install packages

    && apt-get install -y \
           ca-certificates \
           curl \
           gconf2 \
           gconf-service \
           git \
           gtk2-engines-murrine \
           gvfs-bin \
           libasound2 \
           libcanberra-gtk-module \
           libgtk2.0-0 \
           libnotify4 \
           libnss3 \
           libxtst6 \
           python \
           unity-gtk2-module \
           wget \
           xdg-utils \

    # Install atom

    && curl -sLo /tmp/atom.deb "https://github.com/atom/atom/releases/download/v$ATOM_VERSION/atom-amd64.deb" \
    && dpkg -i /tmp/atom.deb \

    # Clean

    && rm -rf \
           /tmp/* \
           /var/lib/apt/lists/*

COPY ./rootfs /

ENTRYPOINT [ "/entrypoint.sh" ]
