FROM golang:1.21

WORKDIR /app

COPY . .

RUN go mod init goapp && \
    go get google.golang.org/grpc && \
    go get google.golang.org/protobuf && \
    go build -o server .

EXPOSE 50051

CMD ["./server"]