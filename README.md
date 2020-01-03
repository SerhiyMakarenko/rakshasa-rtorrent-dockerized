# General
[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](https://github.com/SerhiyMakarenko/rakshasa-rtorrent-dockerized/blob/rakshasa-rtorrent-client/stable/LICENSE)

rTorrent is a text-based ncurses BitTorrent client written in C++, based on the libTorrent libraries for Unix focused on high performance and good code.

# Details
Currently, the image supports the following CPU architectures:
 - x86_64 (amd64);
 - armhf (arm32v6);
 - arm7l (arm32v6);
 - aarch6 (arm64v8).

This means that the image can be used on regular PC's with Intel CPU as well as on single-board computers like Raspberry Pi with ARM CPU.

# Usage
To run container you need to execute command listed below:
```
docker run -d --name rakshasa-rtorrent-client --net=host \
    -v /path/to/rtorrent.rc:/usr/local/etc/rtorrent/rtorrent.rc \
    serhiymakarenko/rakshasa-rtorrent-client:latest
```
Example of the `rtorrent.rc` listed below:
```
scgi_port = 127.0.0.1:5000

system.daemon.set = true
```
