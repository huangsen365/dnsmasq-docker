# dnsmasq-docker
dnsmasq docker

# docker build
docker build -t dnsmasq-docker .

# docker build
docker pull huangsen365/dnsmasq-docker

# docker run
docker run -d --restart=always -p 53:53/tcp -p 53:53/udp --cap-add=NET_ADMIN huangsen365/dnsmasq-docker

docker run -d --restart=always -p 53:53/tcp -p 53:53/udp --cap-add=NET_ADMIN --dns 202.96.134.33 --dns 202.96.128.86 -v /root/mydnsmasq_20190907/etc_dnsmasq.d:/etc/dnsmasq.d -v /root/mydnsmasq_20190907/etc_dnsmasq.conf:/etc/dnsmasq.conf -v /root/mydnsmasq_20190907/dnsmasq_8.log:/var/log/dnsmasq_8.log --name mydnsmasq_20190907_img_c mydnsmasq_20190907_img --log-facility=/var/log/dnsmasq_8.log
