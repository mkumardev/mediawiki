# mediawiki
MediaWiki is a free and open-source wiki engine. It was developed for use on Wikipedia in 2002, and given the name "MediaWiki" in 2003

Aim is to make this app running on a container and database in another container .
just install docker 
clone this repo and run the command
#docker build -t myapp .                   // in your current directory mediawikiapp repo must be cloned to work

#docker build -t mydb .                    // in your current directory mediawikidb repo must be cloned to work



$ docker run -d -v /webroot:/var/www -p 82:80 --name myapp myapp
$ docker run -it --network some-network --rm mariadb mysql -hsome-mariadb -uexample-user -p
$ docker run -it --rm mariadb mysql -hsome.mysql.host -usome-mysql-user -p
