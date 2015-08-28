[![Deploy to Tutum](https://s.tutum.co/deploy-to-tutum.svg)](https://dashboard.tutum.co/stack/deploy/)

BUILD

docker build -t adeo/testlink --rm=true --force-rm=true .

RUN

docker run -d -p 80:80 -p 3306:3306 -v /home/wikeo/testlinkMySQL:/var/lib/mysql --name testlink -e MYSQL_PASS="admin" adeo/testlink

DEBUG

docker run -t -i -p 80:80 -p 3306:3306 --name testlink -e MYSQL_PASS="admin" adeo/testlink /bin/bash
