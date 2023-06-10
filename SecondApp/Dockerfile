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
COPY SecondApp/file1 /app/SecondApp/file1
COPY SecondApp/file2 /app/SecondApp/file2

