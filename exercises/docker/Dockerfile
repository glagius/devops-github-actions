FROM node:16

WORKDIR /fastify_app

COPY ./fastify_app /fastify_app/

RUN npm install

EXPOSE 3000

CMD ["npm", "start"]