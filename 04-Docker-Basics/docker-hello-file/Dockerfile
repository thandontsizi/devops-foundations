# Using Ubuntu as a base image:
FROM Ubuntu

# Update packages (Dependencies and Libraries):
Run apt update

# Create a file inside the container (Environment Configuration):
RUN echo "Hello, Docker!" > /hello.txt

# Default command when the container starts:
CMD ["cat", "/hello.txt"]
