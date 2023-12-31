# GoURL

## Overview
GoURL is a project designed to simplify URL redirection using Docker and Cloudflare Tunnel. GoURL-Server serves as a complementary sub-project designed for effortless deployment.

## Project Structure
GoURL-Server project is organized as follows:

```
GoURL-Server
├── docker-compose.yml
├── data
│   └── url.csv
└── env
    └── cloudflared.env
```

### `docker-compose.yml`
This file contains the Docker Compose configuration necessary to run the GoURL Server. It orchestrates the deployment of the server and other associated services.

### `data/url.csv`
The `url.csv` file, located within the `data` folder, serves as the central storage for the URL redirection table. This file is automatically generated and managed by the program.

### `env/cloudflared.env`
The `cloudflared.env` file, located within the `env` folder, is crucial for configuring the Cloudflare Tunnel service. Users need to create this file manually and populate it with the required environment variables to enable the integration with Cloudflare Tunnel.

## Getting Started
To get started with the GoURL Server project, follow these steps:

1. Clone the repository to your local machine.
2. Create the `env/cloudflared.env` file and configure it with the appropriate Cloudflare Tunnel environment variables. (See `env/example-cloudflared.env`)
3. Use Docker Compose to deploy the GoURL Server by running `docker compose up`.
4. The program will automatically generate and manage the `data/url.csv` file for URL redirection.