FROM golang:1.20
WORKDIR /app
COPY . .
RUN go mod tidy && go mod verify
RUN go test main.go main_test.go -v 
RUN go build -v -o main .
CMD ["/app/main"]
