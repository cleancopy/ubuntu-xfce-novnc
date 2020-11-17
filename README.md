# ubuntu-xfce-novnc

A modified/updated & cleaned version of https://github.com/ConSol/docker-headless-vnc-container for personal use
will setup ubuntu 18.04 with xfce & noVNC and listen on 6901 for web connections.

## Quick start

1. `git clone https://github.com/cleancopy/ubuntu-xfce-novnc.git`
2. `docker build -t cleancopy/ubuntu-xfce-novnc:18.04 .`
3. `docker-compose up -d`
4. `open a browser and go to http://127.0.0.1:6901 or use any VNC client to connect to port 5901`
