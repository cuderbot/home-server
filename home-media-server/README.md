# Home Media Server

Aqui almaceno todo lo relacionado al servicio de `home media server`.

## Servicios

    - Jellyfin: Cliente de archivos media.
        * http://jellyfin:8096
    - Transmission: Cliente de torrents.
        * http://transmission:9091
    - Flexget: Automatizador de tareas varias.
        *  http://flexget:5050/flexget/series

# Requisitos

    - Docker
    - Docker-compose

# Como Instalar

```
# Clonar el repo
git clone https://github.com/cuderbot/home-server.git

# Ir a carpeta `home-media-server`
cd home-media-server/

# Crear una copia de archivo `.env` con variables de configuración
cp .env.example .env
# Crear una copia de archivo `secrets.yml` ubicado en flexget/ con las credenciales de cliente transmission
cp flexget/secrets.example.yml flexget/secrets.yml
# Crear una copia de archivo `anime.yml` ubicado en flexget/ con la lista de animes deseados
cp flexget/anime.example.yml flexget/anime.yml

# Levantar los servicios usando `docker-compose`
docker-compose up -d

# Listo!
```
