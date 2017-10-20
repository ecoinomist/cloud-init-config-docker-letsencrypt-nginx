# Cloud-Init Config with Docker Letsencrypt Nginx Proxy for Digital Ocean Droplet Creation

Simplify the initial setup process when creating new VPS instances in host providers like Digital Ocean, by copy-pasting the user data provided in `cloud-config.yml`. 
Works with droplet creation using Ubuntu 16.04 image.

This config provides:
- Security enhancements ([best practices recommended by Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-use-cloud-config-for-your-initial-server-setup)):
    - Disabled root login
    - Disabled username/password login
    - Create new user with sudo privileges and no password for ease of use
    - Restrict SSH login to using private key, custom username and custom port
    - Enabled Firewall (only ports 80/443 and custom SSH port are open)
- Automatic service/s launch on boot using `/startup.sh`
- Automatic SSL support and renewal (IPV6 included) for domains using [Letsencrypt Nginx Proxy with Docker](https://github.com/ecoinomist/docker-letsencrypt-nginx-proxy)
- Latest Docker and Docker-Compose setup
- Docker command aliases
- Git command aliases

## Usage

Open `cloud-config.yml` and do string search and replace as listed in comments.
