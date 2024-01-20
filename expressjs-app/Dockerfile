FROM node:20

WORKDIR /usr/app/express

COPY . .

# The RUN command is used to execute commands during the image build process.
# clean install
RUN npm ci

EXPOSE 8000

# The CMD command is used to provide default commands for the container to execute when it starts
CMD ["node", "index.js"]
