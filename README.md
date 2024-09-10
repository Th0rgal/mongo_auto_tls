# mongo_auto_tls

A simple Docker Compose configuration to set up a MongoDB instance with automatic SSL certificate generation and renewal.

## Features

- Automatically generates and renews SSL certificates using Let's Encrypt
- Configures MongoDB to use TLS for secure connections
- Easy setup with minimal configuration required

## Prerequisites

- Docker and Docker Compose installed on your system
- A domain name pointed to your server's IP address

## Usage

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/mongo_auto_tls.git
   cd mongo_auto_tls
   ```

2. Edit the `compose.yml` file:
   - Replace `yourdomain.name` with your domain name
   - Update the email address in the certbot command
   - Change the `MONGO_INITDB_ROOT_PASSWORD` to a secure password

3. Start the services:
   ```
   docker compose up -d
   ```

4. Your MongoDB instance will be available on port 27017 with TLS enabled.

## Warning

- **Important:** This configuration uses ports 80 and 443 for the ACME challenge. Ensure these ports are available and not in use by other services on your system.

- The MongoDB version used in this compose file is `8.0.0-rc20`. Please check for the latest stable version and update accordingly in the `compose.yml` file.

## License

[MIT License](LICENSE.md)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
