FROM ubuntu:14.04
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    ATOM_VERSION=1.4.1 \
    CA_CERTIFICATES_VERSION=20141019 \
    CURL_VERSION=7.35.0 \
    DEBIAN_FRONTEND=noninteractive \
    GCONF_VERSION=3.2.6 \
    GIT_VERSION=1.9.1 \
    GTK2_ENGINES_MURRINE=0.98.2 \
    GVFS_VERSION=1.20.3 \
    LIBASOUND2_VERSION=1.0.27.2 \
    LIBCANBERRA_GTK_MODULE=0.30 \
    LIBGTK2_VERSION=2.24.23 \
    LIBNOTIFY_VERSION=0.7.6 \
    LIBNSS3_VERSION=3.19.2 \
    LIBXTST6_VERSION=1.2.2 \
    PYTHON_VERSION=2.7.5 \
    UNITY_GTK2_MODULE=0.0.0 \
    WGET_VERSION=1.15 \
    XDG_VERSION=1.1.0

RUN set -x \

    # Prepare system

    && apt-get update \

    # Install packages

    && apt-get install -y --no-install-recommends \
           ca-certificates=$CA_CERTIFICATES_VERSION* \
           curl=$CURL_VERSION* \
           gconf2=$GCONF_VERSION* \
           gconf-service=$GCONF_VERSION* \
           git=1:$GIT_VERSION* \
           gtk2-engines-murrine=$GTK2_ENGINES_MURRINE* \
           gvfs-bin=$GVFS_VERSION* \
           libasound2=$LIBASOUND2_VERSION* \
           libcanberra-gtk-module=$LIBCANBERRA_GTK_MODULE* \
           libgtk2.0-0=$LIBGTK2_VERSION* \
           libnotify4=$LIBNOTIFY_VERSION* \
           libnss3=2:$LIBNSS3_VERSION* \
           libxtst6=2:$LIBXTST6_VERSION* \
           python=$PYTHON_VERSION* \
           unity-gtk2-module=$UNITY_GTK2_MODULE* \
           wget=$WGET_VERSION* \
           xdg-utils=$XDG_VERSION* \

    # Install atom

    && curl -sLo /tmp/atom.deb "https://github.com/atom/atom/releases/download/v$ATOM_VERSION/atom-amd64.deb" \
    && dpkg -i /tmp/atom.deb \

    # Clean

    && rm -rf \
           /tmp/* \
           /var/lib/apt/lists/*

COPY ./root /

ENTRYPOINT [ "/entrypoint.sh" ]
