FROM debian

RUN apt-get update \
 && apt-get install --yes nginx-light \
 && rm -r /var/cache/apt/ /var/lib/apt/

EXPOSE 80
ENTRYPOINT ["/usr/sbin/nginx", "-g", "daemon off;"]
