FROM node:alpine

WORKDIR '/usr/fib'

COPY ./package.json ./
RUN npm install

COPY ./ ./

RUN npm run build

FROM nginx:alpine
EXPOSE 3000

COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf

COPY --from=0 /usr/fib/build /usr/share/nginx/html
