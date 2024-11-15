# netflix-at-home

A nearly fully preconfigured, Docker-based [*arr-stack](https://wiki.servarr.com/) and [Jellyfin](https://jellyfin.org/) setup for seamless streaming of movies, TV shows, music, and books.

## Usage
- Use **Jellyfin** to view media.
- Add new media using **Radarr (movies)**, **Sonarr (shows)**, **Lidarr (movies)**, or **Readarr (books)**. 

## Web Endpoints
- [Jellyfin (Media server)](http://localhost:8096/)

- [Bazarr (Subtitles)](http://localhost:6767/)
- [Radarr (Movies)](http://localhost:7878/)
- [Sonarr (Shows)](http://localhost:8989/)

- [Lidarr (Music)](http://localhost:8686/)

- [Readarr (Books)](http://localhost:8787/)

- [Prowlarr (Indexers)](http://localhost:9696/)
- [qBittorrent (Download client)](http://localhost:8080/)

## Default Credentials
- Username: `hey`
- Password: `lemmein`

## Prerequisites
- ### Docker
    - Must be ran with the WSL 2 backend if on Windows. Please refer to: [Docker WSL 2](https://docs.docker.com/desktop/features/wsl/).

## Installation
1. Clone this repo.
2. Run `docker-compose up -d --remove-orphans`.

## Configuration

- ### Bazarr
    1. Create a free account at [opensubtitles.com](https://www.opensubtitles.com/).
    2. navivgate to [localhost:6767/settings/providers](http://localhost:6767/settings/providers/).
    3. Add the provider `OpenSubtitles.com` and enter the credentials of your account.

- ### Jellyfin
    - Configure hardware acceleration under `Dashboard > Playback > Transcoding`. (Optional)
        - [Linux host with AMD GPU](https://jellyfin.org/docs/general/administration/hardware-acceleration/amd#configure-with-linux-virtualization).
        - [Linux host with Nvidia GPU](https://jellyfin.org/docs/general/administration/hardware-acceleration/nvidia#configure-with-linux-virtualization).
        - [Windows host with AMD GPU](https://jellyfin.org/docs/general/administration/hardware-acceleration/amd#configure-on-windows-host).
        - [Windows host with Nvidia GPU](https://jellyfin.org/docs/general/administration/hardware-acceleration/nvidia/#configure-with-linux-virtualization).
        - [Other](https://jellyfin.org/docs/general/administration/hardware-acceleration/)
