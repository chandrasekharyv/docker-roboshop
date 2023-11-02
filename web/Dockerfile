FROM nginx
RUN rm -rf /usr/share/nginx/html/index.html
RUN rm -rf /etc/nginx/conf.d/default.d
RUN rm -rf /etc/nginx/nginx.conf
COPY roboshop.conf /etc/nginx/roboshop.conf
ADD static /usr/share/nginx/html/