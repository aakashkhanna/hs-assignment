FROM node:18-alpine AS build

WORKDIR /app

COPY package*.json ./

COPY tsconfig*.json ./

RUN npm install

COPY . .

RUN npm run build

FROM node:18-slim

WORKDIR /app

COPY --from=build /app/dist ./dist

COPY --from=build /app/package*.json ./

COPY --from=build /app/tsconfig*.json ./

RUN npm install

CMD [ "npm", "run", "start:dev" ]