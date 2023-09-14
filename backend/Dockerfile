FROM node:13.8.0

WORKDIR /app

COPY . .


ENV TYPEORM_CONNECTION=postgres
ENV TYPEORM_HOST=db
ENV TYPEORM_PORT=5432
ENV TYPEORM_USERNAME=postgres
ENV TYPEORM_PASSWORD=password
ENV TYPEORM_DATABASE=glee
ENV TYPEORM_MIGRATIONS=./src/migrations/*.ts
ENV TYPEORM_ENTITIES=./src/modules/**/*.entity.ts
RUN npm install
RUN npm run build
# RUN npm run migrations
# CMD ["npm", "start"]

CMD npm run migrations && npm start

