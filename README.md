# dnsmasq-docker
dnsmasq docker

# docker build
docker build -t dnsmasq-docker .

# docker fun
docker run -d --restart=always -p 53:53/tcp -p 53:53/udp --cap-add=NET_ADMIN dnsmasq-docker
