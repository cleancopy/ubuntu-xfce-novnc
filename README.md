# ubuntu-xfce-novnc

A modified/updated & cleaned version of https://github.com/ConSol/docker-headless-vnc-container for personal use
will setup ubuntu 18.04 with xfce & noVNC and listen on 6901 for web connections.

## Quick start

1. `git clone https://github.com/cleancopy/ubuntu-xfce-novnc.git`
2. Edit the Dockerfile to set username, password
3. Edit ./src/ubuntu/install/tools.sh to add extra packages (where sudo and nano are)
4. `docker build -t cleancopy/ubuntu-xfce-novnc:18.04 .`
5. `docker-compose up -d`
6. `open a browser and go to http://127.0.0.1:6901 or use any VNC client to connect to port 5901`

## Even Quicker start

1. `git clone https://github.com/cleancopy/ubuntu-xfce-novnc.git`
2. `docker-compose up -d`
3. `open a browser and go to http://127.0.0.1:6901 or use any VNC client to connect to port 5901`
4. Log in with password 'password' (without quotes)

## I don't even want to have a compose file

1. `docker run -p 80:6901 cleancopy/ubuntu-xfce-novnc`
2. `open a browser and go to http://127.0.0.1 or use any VNC client to connect to port 5901`

## Changing some settings (password, resolution)

1. `docker run -p 8080:6901 -e VNC_RESOLUTION=1920x1080 -e VNC_PW=newpassword cleancopy/ubuntu-xfce-novnc`
2. `open a browser and go to http://127.0.0.1:8080 or use any VNC client to connect to port 5901`

### Additional info

Windows Docker desktop likes to keep the container running even after hitting ctrl-c to kill it - adding -t -i on the command line seems to prevent this behaviour
e.g.

`docker run -i -t -p 8080:6901 -e VNC_RESOLUTION=800x600 -e VNC_PW=password cleancopy/ubuntu-xfce-novnc`
