# Nginx RTMP server

Debian Stretch based container of Nginx streaming server with RTMP patch.

## Parameters of Nginx

List of parameters:

    Path prefix: "/opt/nginx"
    Binary file: "/opt/nginx/sbin/nginx"
    Modules path: "/opt/nginx/modules"
    Configuration prefix: "/opt/nginx/etc"
    Configuration file: "/opt/nginx/etc/nginx.conf"
    Pid file: "/opt/nginx/logs/nginx.pid"
    Error log file: "/opt/nginx/logs/error.log"
    Http access log file: "/opt/nginx/logs/access.log"

## Example of docker-compose.yml

    mysql:
      image: evilfreelancer/nginx-rtmp:latest
      ports:
        - "80:80"
        - "1935:1935"
      volumes:
        - ./configs:/opt/nginx/etc
        - ./logs:/opt/nginx/logs

# Links

* https://nginx.org/download/
* https://github.com/arut/nginx-rtmp-module
* https://ffmpeg.org/releases/
