# How to use this image

start webdav server
> $ docker-compose up

stop webdav server
> $ docker-compose down

## docker environment

* access point
  - Then access it via http://localhost:80 or http://host:80 in a browser.
* used port
  - The webdav server listening on the default port of 80.
* media folder: ./media - served directory
  - This server will serve files located in your ./media folder
* authorized user/password
  - To restrict access to only authorized users, you can define two environment variables: USERNAME and PASSWORD in docker-compose.yml
> $ docker run --name webdav -p 80:80 -v /media:/media -e USERNAME=webdav -e PASSWORD=webdav -d hephaex/webdav
