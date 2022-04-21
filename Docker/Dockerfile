FROM golang:alpine AS builder

# Set necessary environmet variables needed for our image
ENV SENDER_EMAIL=SENDER@TEST.COM \
    PASSWORD=PASSWORD \
    RECEIVER_EMAIL=RECIVER@TEST.COM

# Move to working directory /app
WORKDIR /app

# Copy and download dependency using go mod
COPY go.mod .
COPY go.sum .
RUN go mod download

# Copy the code into the container
COPY . .

# CGI has to be disabled for alpine and Build the application
RUN export CGO_ENABLED=0 && go build -o mainGo .

# Move to /dist directory as the place for resulting binary folder
WORKDIR /dist

# Copy binary from build to mainGo folder
RUN cp /app/mainGo .

# Build a small image
FROM scratch

COPY --from=builder /dist/mainGo /

# Command to run
ENTRYPOINT ["/mainGo"]
