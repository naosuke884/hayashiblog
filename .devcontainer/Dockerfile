FROM node:20.6.1-slim
EXPOSE 8889
RUN apt update && apt install -y \
    curl \
    git \
    vim
RUN npm install -g pnpm

COPY .. /app

WORKDIR /app

RUN pnpm install
