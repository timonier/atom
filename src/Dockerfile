FROM ubuntu:16.04

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

ENV \
    ATOM_VERSION=1.7.4 \
    NO_AT_BRIDGE=1

RUN set -x \

    # Prepare system

    && export DEBIAN_FRONTEND=noninteractive \

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
           libatk-adaptor \
           libcanberra-gtk-module \
           libgail-common \
           libgtk2.0-0 \
           libnotify4 \
           libnss3 \
           libxtst6 \
           overlay-scrollbar-gtk2 \
           python \
           unity-gtk2-module \
           wget \
           xdg-utils \

    # Install atom

    && curl -sLo /tmp/atom.deb "https://github.com/atom/atom/releases/download/v${ATOM_VERSION}/atom-amd64.deb" \
    && dpkg -i /tmp/atom.deb \

    # Install timonier/dumb-entrypoint

    && curl -sL "https://github.com/timonier/dumb-entrypoint/raw/master/bin/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s install \

    # Clean

    && rm -rf \
           /tmp/* \
           /var/lib/apt/lists/*

ENTRYPOINT [ "dumb-init" , "--" , "dumb-entrypoint" ]
