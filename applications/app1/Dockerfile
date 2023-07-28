FROM node:16

WORKDIR /app

COPY applications/app1/package.json applications/app1/package.json
COPY applications/app1/package-lock.json applications/app1/package-lock.json
RUN cd applications/app1
RUN ls -alR
WORKDIR /app/applications/app1
RUN npm install

WORKDIR /app
COPY . .
WORKDIR /app/applications/app1
RUN npm run build

CMD ["npm", "run", "start"]