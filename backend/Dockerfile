FROM node:22-alpine

WORKDIR /app

COPY package.json ./
COPY backend/package.json ./backend/package.json
COPY frontend/package.json ./frontend/package.json

RUN npm install

COPY backend ./backend

RUN npm run build:backend

EXPOSE 5000

CMD ["npm", "run", "start", "--workspace", "backend"]
