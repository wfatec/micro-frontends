FROM node:11

# Create app directory
RUN mkdir -p /code
WORKDIR /code

# Install app dependencies
COPY package.json /code/
# RUN npm install
COPY ./node_modules /code/node_modules
COPY webpack.config.js /code/

# Bundle app source
COPY ./src /code/src

EXPOSE 3001
CMD [ "./node_modules/.bin/nodemon", "--watch", "./src", "--exec", "npm", "start" ]