# rtspWatchdog

Reboots an ONVIF/RTSP camera if RTSP is down. VStarcam cameras suffer from this problem.

Python must be >= 3.6

# Usage

```
git clone https://github.com/lucaszanella/rtspWatchdog
cd dev
sudo docker build -t rtspwatchdog .
sudo docker run -v $(pwd)/..:/home -d --restart unless-stopped -it --name rtspwatchdog rtspwatchdog
```

Tip: follow the log on a screen:

`screen`

then leave open:

`sudo docker logs --follow rtspwatchdog`

Reattach to screen with `screen -r -d`

# Raspberry pi

See here a list of base images and substitute in the dockerfile: https://www.balena.io/docs/reference/base-images/base-images-ref/
