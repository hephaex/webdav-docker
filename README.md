[![License](https://img.shields.io/badge/license-GPL-blue.svg)](https://raw.githubusercontent.com/hephaex/webdav-docker/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/hephaex/webdav.svg)](https://hub.docker.com/r/hephaex/webdav/)
[![Docker Stars](https://img.shields.io/docker/stars/hephaex/webdav.svg)](https://hub.docker.com/r/hephaex/webdav/)
[![Build Status](https://travis-ci.org/hephaex/webdav-docker.svg?branch=master)](https://travis-ci.org/hephaex/webdav-docker)
[![Bitcoin donate button](https://img.shields.io/badge/bitcoin-donate-yellow.svg)](https://www.coinbase.com/checkouts/16wBMRsdZkNu6Vk7zQetX27aHLnvwusedz)

# How to use this image

start webdav server
> $ docker-compose up -d

stop webdav server
> $ docker-compose down

## docker environment

* access point
  - Then access it via http://localhost:80 or http://host:80 in a browser.
* used port
  - The webdav server listening on the default port of 80.
* media folder:
  - /media - served directory
  - This server will serve files located in your /media folder
* authorized user/password in folder
  - To restrict access to only authorized users, 
  - you can define two environment variables: 
  - USERNAME and PASSWORD in docker-compose.yml
* docker run 
> $ docker run --name webdav -p 80:80 -v /media:/media -e USERNAME=webdav -e PASSWORD=webdav -d hephaex/webdav
