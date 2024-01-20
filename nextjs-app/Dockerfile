FROM node:20

WORKDIR /usr/app/next

COPY . .

# The RUN command is used to execute commands during the image build process.
# clean install
RUN npm ci

RUN npm run build

EXPOSE 3000

# The CMD command is used to provide default commands for the container to execute when it starts
CMD ["npm", "start"]
