FROM node:argon

RUN npm install pm2 -g

VOLUME ["/var/www/example.com/api"]

ADD start.sh /start.sh

RUN chmod 755 /start.sh

EXPOSE 8080
CMD ["/start.sh"]

# docker build -t benben/node-dev .
