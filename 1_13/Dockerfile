FROM golang:1.16
WORKDIR /usr/app/src
COPY . .
RUN go build .
EXPOSE 8080
ENTRYPOINT [ "./server" ]