FROM node:alpine

WORKDIR '/usr/fib'

COPY ./package.json ./
RUN npm install

COPY ./ ./

CMD ["npm", "run", "start"]
