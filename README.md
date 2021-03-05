# lancache
  $sudo docker pull lancachenet/monolithic
  
  $sudo docker run --network mynet --name lancache -detach -v /srv/pool/cache:/data/cache -v /srv/pool/cache/logs:/logs/cache -p 80:80 lancachenet/monolithic:latest

# lancache-dns
  $sudo docker pull lancachenet/lancache-dns
  
  $sudo docker run --network mynet --name lancache-dns -detach -p 53:53/udp -e USE_GENERIC_CACHE=TRUE -e LANCACHE_IP=192.168.2.4 lancachenet/lancache-dns:latest

