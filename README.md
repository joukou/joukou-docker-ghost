## Ghost Dockerfile

[![Build Status](https://circleci.com/gh/joukou/joukou-docker-ghost/tree/develop.png?circle-token=5da93a9fd8a8ff8a1bc69f6942a1435d5fbf2029)](https://circleci.com/gh/joukou/joukou-docker-ghost/tree/develop) [![Docker Repository on Quay.io](https://quay.io/repository/joukou/ghost/status?token=5a034dc7-bed9-4835-89ef-864fe1370442 "Docker Repository on Quay.io")](https://quay.io/repository/joukou/ghost) [![Proprietary](http://img.shields.io/badge/license-proprietary-red.svg)](#license)

[Ghost](https://www.ghost.org/) Dockerfile.

### Base Docker Image

* [quay.io/joukou/nodejs](https://github.com/joukou/joukou-docker-nodejs)

### Usage

    docker run -d -p 80:2368 quay.io/joukou/ghost

#### Customizing Ghost

    docker run -d -p 80:2368 -v <override-dir>:/ghost-override quay.io/joukou/ghost

where `<override-dir>` is an absolute path of a directory that could contain:

  - `config.js`: custom config file copied from [here](https://github.com/TryGhost/Ghost/blob/master/config.example.js) (you must replace `127.0.0.1` with `0.0.0.0`)
  - `content/data/`: persistent/shared data
  - `content/images/`: persistent/shared images
  - `content/themes/`: more themes

After few seconds, open `http://<host>` for blog or `http://<host>/ghost` for admin page.

### License

Derived from https://github.com/dockerfile/ghost under the terms of the MIT
license.

Copyright &copy; Joukou Ltd. All rights reserved.