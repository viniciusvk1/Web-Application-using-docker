FROM node:12-alpine
WORKDIR /app
COPY package.json .
RUN apk add --no-cache python2 g++ make
RUN yarn install --production
COPY . .
CMD ["node", "src/index.js"]
EXPOSE 3000

# Adding a new user -> RUN addgroup dev && adduser -S -G "name" dev
# Switching to the user created -> USER "name"
# CMD -> docker run -dp 3000:3000 app