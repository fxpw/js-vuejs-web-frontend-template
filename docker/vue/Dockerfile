FROM node:22 AS builder

WORKDIR /app

# COPY package.json package-lock.json ./

# RUN npm install

# COPY . .
# RUN npm run build
EXPOSE 8080 5173
COPY ./docker-entrypoint.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/docker-entrypoint.sh
RUN ln -s /usr/local/bin/docker-entrypoint.sh /

ENTRYPOINT ["docker-entrypoint.sh"]