#################################################################
# Dockerfile para construir imágenes de contenedores de Zimbra Collaboration 8.7.11
# Basado en Ubuntu 16.04
#################################################################
FROM ubuntu:16.04
MAINTAINER gmorochom <gmorochom987@gmail.com>

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get -y install \
  wget \
  openssh-client \
  bind9 \
  bind9utils \
  bind9-doc \
  dnsutils \
  libidn11 \
  libpcre3 \
  libgmp10 \
  libexpat1 \
  libstdc++6 \
  libperl5.18 \
  libaio1 \
  netcat-openbsd \
  pax \
  resolvconf \
  sqlite3 \
  sudo \
  sysstat \
  unzip

VOLUME ["/opt/zimbra"]

EXPOSE 22 25 465 587 110 143 993 995 80 443 8080 8443 7071

COPY opt /opt/

COPY etc /etc/

CMD ["/bin/bash", "/opt/start.sh", "-d"]
