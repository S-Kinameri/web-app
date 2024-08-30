FROM nginx:1.23.3 AS production
COPY ./infra/nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./infra/nginx/default.conf /etc/nginx/conf.d/default.conf
COPY ./src /data

#FROM production AS local
#RUN sed -i -e s/127.0.0.1:9000/app:9000/ /etc/nginx/conf.d/default.conf

#CMD ["/bin/sh", "-c", "envsubst '${PHP_HOST}' < /etc/nginx/conf.d/default.conf > /etc/nginx/conf.d/default.conf.tmp && mv /etc/nginx/conf.d/default.conf.tmp /etc/nginx/conf.d/default.conf && nginx -g 'daemon off;'"]