FROM node:18-alpine


WORKDIR /app
COPY package*.json .
RUN npm install
COPY . .
ENV VITE_HOST=0.0.0.0
ENV VITE_PORT=5173
RUN npm run build
EXPOSE 5173
CMD ["npm", "run", "dev"]

