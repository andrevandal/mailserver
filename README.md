# Mailserver

This repository provides the necessary structure for setting up and maintaining an email server using `docker-compose` for my personal use. However, it also serves as a reference for knowledge sharing with the community.

Check out the `docker-compose.yml` file for a comprehensive configuration.

Our stack includes:
- Docker-mailserver (https://docker-mailserver.github.io/docker-mailserver/latest/)
- Cloudflare as the DNS server
- Certbot with DNS challenge and automatic certificate renewal

You can also find an example setup for Docker-Mailserver with Certbot DNS Cloudflare in the [official documentation](https://docker-mailserver.github.io/docker-mailserver/latest/config/security/ssl/#example-using-certbot-dns-cloudflare-with-docker).

## Prerequisites

- Docker and docker-compose installed
- Cloudflare account with the relevant API token

## Usage

1. Clone this repository:

```sh
git clone https://github.com/andrevandal/mailserver
```

2. Navigate to the project directory and edit the `docker-data/certbot/secrets/cloudflare.ini` file, inserting your Cloudflare API token.

3. Update the domain variables (such as `domainname` and `-d`) according to your preferences and Cloudflare settings.

4. Start the docker-compose:

```sh
docker-compose up -d
```

5. (Optional) Use the `setup.sh` script to assist in configuring your email server. See the instructions inside the `setup.sh` file.

## License

This project is licensed under the MIT License.

## Contributions

Contributions and suggestions are welcome through Pull Requests.

## Issues

If you encounter any issues or have questions, please feel free to open an issue at the following link: https://github.com/andrevandal/mailserver/issues

Thank you for your interest and support in this project!