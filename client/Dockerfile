FROM node:16-alpine as builder
WORKDIR '/app'
COPY ./package.json ./
RUN npm install 
COPY . .
#Generate the static files of the page
RUN npm run build


#Serve the static file into nginx
FROM nginx 
EXPOSE 3000
COPY nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html



