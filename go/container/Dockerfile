FROM golang:alpine3.16

RUN mkdir /app
ADD ./app /app/
WORKDIR /app
RUN go mod download
RUN go build -o main .

EXPOSE 8080
CMD ["/app/main"]