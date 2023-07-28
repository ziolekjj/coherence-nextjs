FROM node:16

WORKDIR /app


COPY applications/app2/package.json applications/app2/package.json
COPY applications/app2/package-lock.json applications/app2/package-lock.json
RUN cd applications/app2
RUN npm install

COPY . .
RUN npm run build

CMD ["npm", "run", "start"]