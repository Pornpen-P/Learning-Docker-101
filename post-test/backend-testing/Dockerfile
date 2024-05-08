FROM node:alpine
RUN npm install -g newman newman-reporter-htmlextra
WORKDIR /etc/newman
COPY  . .
ENTRYPOINT ["sh", "./entrypoint.sh"]
CMD [ "newman", "run", "third_party.postman_collection", "-r", "htmlextra,cli,junit" ]

FROM node:alpine
RUN npm install -g newman newman-reporter-htmlextra
WORKDIR /etc/newman
COPY  . .
ENTRYPOINT ["sh", "./entrypoint.sh"]
CMD [ "newman", "run", "backend1.postman_collection.json", "-r", "htmlextra,cli,junit" ]

FROM node:alpine
RUN npm install -g newman newman-reporter-htmlextra
WORKDIR /etc/newman
COPY  . .
ENTRYPOINT ["sh", "./entrypoint.sh"]
CMD [ "newman", "run", "backend2.postman_collection.json", "-r", "htmlextra,cli,junit" ]

