FROM ubuntu
RUN apt update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt install -y nodejs
WORKDIR /usr/src/app
COPY . .
RUN node -v && npm -v && npm install
RUN npm install -g serve
RUN npm run build
EXPOSE 5001
CMD ["-s", "-l", "5001", "build"]
ENTRYPOINT [ "serve" ]
