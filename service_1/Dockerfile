FROM golang:1.20-alpine

WORKDIR /app

COPY go.mod ./
# No need to copy go.sum
RUN go mod download

COPY . .

RUN go build -o main .

EXPOSE 8001

CMD ["./main"]

