FROM node:16.15-alpine AS builder

WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . ./

RUN npm run build \
  && rm -rf ./src \
  && rm -rf node ./node_modules

FROM nginx:1.25.1-alpine AS frontend
WORKDIR /app
COPY --from=builder /app/build /usr/share/nginx/html
COPY ./nginx/conf.d/default.conf /etc/nginx/conf.d

CMD [ "nginx", "-g", "daemon off" ]