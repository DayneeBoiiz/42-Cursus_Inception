FROM debian:buster

RUN apt-get update -y;\
	apt-get install nginx openssl -y

RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/sayar.key -out /etc/ssl/sayar.crt \
	-subj "/C=MA/ST=Khouribga/L=Khouribga/O=42 School/OU=sayar/CN=sayar.42.fr"

COPY conf/nginx.conf /etc/nginx/sites-available/default

CMD [ "nginx", "-g", "daemon off;" ]