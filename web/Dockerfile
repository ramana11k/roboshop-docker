FROM nginx
RUN rm -rf /usr/share/nginx/html/index.html
COPY roboshop.conf /etc/nginx/default.d/roboshop.conf
ADD satic /usr/share/nginx/html/