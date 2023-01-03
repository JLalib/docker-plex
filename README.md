# docker-plex
docker-compose Plex
Instalar Plex en Docker

Cómo instalar Plex en Docker. Disfruta de un centro multimedia al completa, tus series y películas favoritas y mucho más gracias a Plex.

Enlace al docker-compose.yml personalizado con Red propia.

docker-compose.yml
 
---
version: "2.1"
services:
  plex:
    image: lscr.io/linuxserver/plex:latest
    container_name: plex
    network_mode: host
    environment:
      - PUID=1000
      - PGID=1000
      - VERSION=docker
      - PLEX_CLAIM= #optional
    volumes:
      - /path/to/library:/config
      - /path/to/tvseries:/tv
      - /path/to/movies:/movies
    restart: unless-stopped


Vea el vídeo en Youtube.
