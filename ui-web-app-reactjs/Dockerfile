
FROM  node:8

LABEL maintainer ="okoro mellitus"

RUN useradd ui

WORKDIR /app

RUN chown ui /app

COPY . .

RUN npm install

EXPOSE 8080

USER ui

CMD [ "npm","start" ]