#### Docker file nodejs pm2 
FROM cowpanda/alpine-node-pm2:latest
MAINTAINER letrung910@gmail.com

EXPOSE 8080
ENV nodejsapp /app
#RUN mkdir $nodejsapp
WORKDIR $nodejsapp
ADD ./code $nodejsapp
#RUN pm2 start $nodejsapp/hello1.js
#VOLUME /home/trunglv/composenodejs/nodejs/code /app
CMD pm2 start --no-daemon hello1.js 
