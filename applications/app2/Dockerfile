FROM node:16

WORKDIR /app

RUN cd applications/app2

COPY package.json package.json
COPY package-lock.json package-lock.json
RUN npm install

COPY . .
RUN npm run build

CMD ["npm", "run", "start"]