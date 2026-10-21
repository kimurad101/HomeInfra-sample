##以下はマルチアーキテクチャ対応のために「buildx」を使用する文字列(要別途構築)
#FROM --platform=$BUILDPLATFORM debian:trixie-slim AS builder

FROM debian:trixie-slim

RUN echo "deb http://deb.debian.org/debian trixie-backports main contrib" >> /etc/apt/sources.list
RUN apt-get update && apt-get upgrade -y && apt-get -t trixie-backports -y --no-install-recommends install kea-dhcp4-server kea-admin mariadb-client nano iputils-ping iproute2 && apt-get clean

WORKDIR /run/kea
WORKDIR /etc/kea/creds
WORKDIR /etc/kea/control/primary
WORKDIR /etc/kea/control/standby
WORKDIR /etc/kea/setup
WORKDIR /etc/kea/ha/primary
WORKDIR /etc/kea/ha/standby
WORKDIR /etc/kea/db
WORKDIR /etc/kea

EXPOSE 67/udp 68/udp
EXPOSE 8004 8005
ENTRYPOINT ["/usr/sbin/kea-dhcp4","-c","/etc/kea/kea-dhcp4.conf"]
