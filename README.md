# Home theather PC Server
Simple home theather PC running on top of docker

## List of included apps
- deluge
- jackett
- nzbget
- sonarr
- radarr
- plex-server
- bazarr
- portainer
- lidarr
- samba

## Running the apps
Create env config file
```sh
cp .env.example .env
```

Modify the .env file
```
# Your timezone, https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
TZ=Asia/Jakarta
# UNIX PUID and PGID, find with: id $USER
PUID=0
PGID=0
# The directory where data and configuration will be stored.
ROOT=/mnt/shade
```

Spin up the containers
```sh
docker-compose up -d
```

## Credits
[sebgl/htpc-download-box](https://github.com/sebgl/htpc-download-box)
