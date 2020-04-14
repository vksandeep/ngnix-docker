
Standard OSS Image of NGINX on local doker

	docker run --name mynginx1 -p 80:80 -d nginx

Access http://localhost:80/ and Test

Copy the default conf and html files for you to edit

	docker cp mynginx1:/usr/share/nginx/html .
	mkdir conf
	docker cp mynginx1:/etc/nginx/conf.d/default.conf conf/ngnix.conf

Remove the nginx container
	docker rm -f mynginx1


Edit your html and configs - Local
Create the docker file

	docker build -t my-nginx .

	docker run -dit --name my-nginx-app -p 80:80 my-nginx


Access http://localhost:80/