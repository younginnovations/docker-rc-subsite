## ResourceContracts Subsite Dockerfile

This repository contains the Dockerfile of [ResouceContracts subsites](https://github.com/younginnovations/resourcecontracts-rc-subsite) for Docker.

### Base Docker Image

[Ubuntu 14.04](http://dockerfile.github.io/#/ubuntu)

### Installation

1. Install [Docker](https://www.docker.com/).
2. Clone this repo `git clone https://github.com/younginnovations/docker-rc-subsite.git`
3. Go to the cloned folder `docker-rc-subsite`
4. Copy `conf/.env.example` to `conf/.env` with configurations
    For olc subsite, write category=olc in .env, category=rc for rc subsites
    You need database configuration as well to save the static content pages
5. Build an image from Dockerfile `docker build -t=subsite .`

### Usage

* Run `docker run -p 80:80 -d subsite`
* Access the system from the browser at http://xxx/site/public/

### TODO

* Update the apache configuration so that the system could be accessed from the base IP http://xxx 
* Mount the system temporary folder to the host folder to preserve the temporary files and logs
* Currently system is run using root, need to use appropriate users for running the servers and applications.