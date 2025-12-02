FROM node:20
WORKDIR /app/server
COPY package.json .
COPY *.js .
EXPOSE 8080
RUN npm install
ENV REDIS_HOST="redis" \
    CATALOGUE_HOST="catalouge" \
    CATALOGUE_PORT=8080
CMD ["node", "server.js"]