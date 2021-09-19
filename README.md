# Home theather PC Server
Simple home theather PC running on top of docker

## List of included apps
- deluge
- jackett
- sonarr
- radarr
- plex-server
- bazarr
- lidarr
- samba

## Running the apps
Create env config file
```sh
cp .env.example .env
```

Modify the .env file
```sh
# Your timezone, https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
TZ=Asia/Jakarta
# UNIX PUID and PGID, find with: id $USER
PUID=0
PGID=0

# The directory where data and configuration will be stored.
DOWNLOAD_ROOT=/mnt/join
CONFIG_ROOT=/work/htpc-config

# Samba configuration
SAMBA_USERNAME=ibnuh
SAMBA_SHARE_COMPLETE=Ubuntu
SAMBA_SHARE_HOME=Ibnuh
SAMBA_PASSWORD=password567
```

Spin up the containers
```sh
docker-compose up -d
```

## Credits
[sebgl/htpc-download-box](https://github.com/sebgl/htpc-download-box)
