FROM node:13.8.0 AS Build
ENV  API_URL=http://backend:3030
RUN git clone https://github.com/medoston/node-app-Devops.git
WORKDIR  /node-app-Devops/frontend
RUN npm install
RUN npm run build

FROM nginx
WORKDIR /usr/share/nginx/html
COPY --from=Build DevOps-proj/frontend/dist .



