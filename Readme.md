# Simple Docker Container Auto Deployment
This is a quick and easy setup to deploy our latest stable versions of the back- and frontend of turnie.re
It works by using Watchtower to automatically redeploy our containers as soon as there is a new version available.

## Installation

1. Clone this repository to the desired folder on the machine you want to deploy
1. Edit following files: 
    - `traefik/traefik.toml` needs the urls for Letsencrypt certificates
    - `turniere-backend.env` needs the correct RAILS_MASTER_KEY to decrypt the saved credentials
    - `turniere-frontend.env` needs the URL under which the backend is publicly available
    - `docker-compose.yml` needs the correct labels corresponding to the URLS for the back- and frontend containers
1. Run `docker-compose up -d`
1. Be happy
