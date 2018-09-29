General Usage:
sudo docker run -d -p 80:80 -v /data/playstrap/quickrun:/var/www -t dbface/apache-php

Using Traefik Router:
sudo docker run -d --label traefik.port=80 --label traefik.frontend.rule="Host:quickrun.playstrap.com" -v /data/playstrap/quickrun:/var/www -t dbface/apache-php