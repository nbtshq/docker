FROM nginx:1.18

LABEL maintainer="NorthernBytes Ab Oy <contact@nbts.fi>"

COPY default.conf.template /etc/nginx/conf.d/

WORKDIR /var/www

EXPOSE 80

CMD /bin/bash -c "envsubst < /etc/nginx/conf.d/default.conf.template > /etc/nginx/conf.d/default.conf \	
			&& nginx -g 'daemon off;'"