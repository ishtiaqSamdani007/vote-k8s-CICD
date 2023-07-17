# Use an official Go runtime as the base image
FROM golang:1.17-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the Go module files and download dependencies
COPY go.mod go.sum ./
RUN go mod download

# Copy the rest of the application source code
COPY . .

# Build the Go application
RUN go build -o myapp

# Expose a port if your application listens on a specific port
EXPOSE 8080

# Run the Go application when the container starts
CMD ["./myapp"]
