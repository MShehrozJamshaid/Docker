FROM golang:1.19-alpine AS build

WORKDIR /app

COPY . .

RUN go mod download

CMD ["go", "run", "./main.go"]

