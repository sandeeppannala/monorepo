FROM ubuntu AS builder

WORKDIR /app

# Copy the 'Modules' directory
COPY Modules /app/Modules

# Build your application using the 'Modules' directory

# Final image
FROM ubuntu

RUN mkdir /app
WORKDIR /app

# Copy application files from the builder stage
COPY --from=builder /app /app

# Copy additional application files
COPY FirstApp/file1 /app/FirstApp/file1
COPY FirstApp/file2 /app/FirstApp/file2

