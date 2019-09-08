Bootstrap: docker
From: ubuntu:18.04

%environment
PATH=/usr/local/src/minimap2-2.17_x64-linux:$PATH
export LC_ALL=C.UTF-8
export LANG=C.UTF-8

%post
sed -i "s/archive.ubuntu/de.archive.ubuntu/" /etc/apt/sources.list && \
sed -i "s/security.ubuntu/de.security.ubuntu/" /etc/apt/sources.list && \
apt-get update
apt-get dist-upgrade -y 
apt-get install wget build-essential unzip git -y 
rm -rf /var/lib/apt/lists/*
mkdir -p /usr/local/src
cd /usr/local/src && \
wget -c https://github.com/lh3/minimap2/releases/download/v2.17/minimap2-2.17_x64-linux.tar.bz2 && \
tar xf minimap2-2.17_x64-linux.tar.bz2 && \
rm minimap2-2.17_x64-linux.tar.bz2

%labels
MAINTAINER BioBox
Version v1.0
