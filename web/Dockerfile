FROM nginx
RUN rm -rf /usr/share/nginx/html/index.html
RUN rm -rf /usr/share/nginx/html/nginx.conf
RUN rm -rf /usr/share/nginx/html/conf.d/default.conf
COPY roboshop.conf /etc/nginx/nginx.conf
ADD static /usr/share/nginx/html/