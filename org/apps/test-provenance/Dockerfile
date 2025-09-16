FROM docker.io/node:lts-alpine

ENV HOST=0.0.0.0
ENV PORT=3000

WORKDIR /app

COPY dist .

RUN npm --omit=dev -f install

CMD [ "node", "main.js" ]
