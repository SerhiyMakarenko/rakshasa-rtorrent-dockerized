# General
[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](https://github.com/SerhiyMakarenko/rakshasa-rtorrent-dockerized/blob/rakshasa-rtorrent-client/stable/LICENSE)

rTorrent is a text-based ncurses BitTorrent client written in C++, based on the libTorrent libraries for Unix focused on high performance and good code.

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