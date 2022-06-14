# imgproxy

A simple docker orchestration to create a caching [imgproxy](https://imgproxy.net/)

## Requirements

- [docker](https://www.docker.com/)
- [docker compose](https://docs.docker.com/compose/)

## Setup

- Create a `.env` based off `.env.example` and set appropriate values
- Make sure the configured docker network exists (`docker network create <network-name>`)

## Running

- Start: `docker compose up -d`
- All containers are configured with restart policy `unless-stopped` and will automatically spin up after a system
  restart

## Notes

- Letsencrypt certificate information will be stored in the `letsencrypt/` folder
- Images will be cached in the `cache/` folder

## Links

- [imgproxy](https://imgproxy.net/)
- [NGINX http proxy](https://nginx.org/en/docs/http/ngx_http_proxy_module.html)
