## Dockerfile for the ownCloud [filter-format-server](https://github.com/owncloud/format-filter-server)

This repository contains **Dockerfile** for the  for the [filter-format-server](https://github.com/owncloud/format-filter-server) that can be used with ownCloud to convert documents to different formats.

**Note:** This is built directly with with the master from https://github.com/owncloud/format-filter-server.


### Dependencies

* [node:0.10](https://index.docker.io/u/_/node)

and installs

* open-jdk 7
* [activemq](http://activemq.apache.org/)


### Installation

1. Install [Docker](https://www.docker.io/).

2. Download [trusted build](https://index.docker.io/u/aaukt/owncloud-ffs/) from public [Docker Registry](https://index.docker.io/): `docker pull aaukt/owncloud-ffs`

   (alternatively, you can build an image from Dockerfile: `docker build -t="aaukt/owncloud-ffs" github.com/owncloud/docker-owncloud-ffs`)


### Usage

    docker run -d -p 16080:16080 aaukt/owncloud-ffs

#### Test

    curl --data "Hello World!" http://127.0.0.1:16080/ > hello_world.odt
