FROM node:16 as build

RUN apt-get update && \
    apt-get install -y --no-install-recommends curl tini && \
    rm -rf /var/lib/apt/lists/*
    
WORKDIR /app

COPY package.json yarn.lock .

RUN yarn install

COPY . .

EXPOSE 5173

CMD ["yarn", "dev"]
