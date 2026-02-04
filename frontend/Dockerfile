FROM node:24.13.0-bookworm AS development

WORKDIR /code
COPY package.json /code/package.json
COPY package-lock.json /code/package-lock.json

RUN npm ci

COPY . /code

ENV CI=true
ENV PORT=3000

ENTRYPOINT [ "npm", "start" ]
