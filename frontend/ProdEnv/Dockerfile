FROM node:14-slim as build

WORKDIR /usr/src/app

COPY ./package.json ./
COPY ./yarn.lock ./

RUN yarn install

COPY . .

RUN yarn build

# => Run container
FROM nginx:1.16.0

COPY --from=build /usr/src/app/build /usr/share/nginx/html

RUN rm /etc/nginx/conf.d/default.conf

COPY nginx/nginx.conf /etc/nginx/conf.d

EXPOSE 8000

# Start Nginx server
CMD ["/bin/bash", "-c", "nginx -g \"daemon off;\""]