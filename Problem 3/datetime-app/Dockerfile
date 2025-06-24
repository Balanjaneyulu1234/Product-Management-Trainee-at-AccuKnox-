FROM golang:1.20-alpine
WORKDIR /app
COPY . .
RUN go build -o datetime-app
CMD ["./datetime-app"]
