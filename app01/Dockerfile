FROM golang:alpine

WORKDIR /app

COPY app/go.mod ./
COPY app/main.go ./

RUN go mod download
RUN go mod tidy

RUN go build -o main .

EXPOSE 8081

CMD ["./main"]