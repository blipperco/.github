## Installation

### Pre-requirements

Linux with Docker & docker-compose installed. **You must be able to use docker-compose without `sudo`**

### Get the code

`cd projects && mkdir blipper && cd blipper`

`git clone git@github.com:blipperco/gateway.git`

`git clone git@github.com:blipperco/backend.git`

`git clone git@github.com:blipperco/frontend.git`

### Install dependencies

`cd gateway && docker-compose up -d && cd ../`

`cd backend && vendor/bin/sail up -d && cp .env.example .env`

`vendor/bin/sail composer install`

`vendor/bin/sail php artisan migrate`

`cd ../frontend && docker-compose run --rm frontend-node-cli yarn install`

`docker-compose up -d`

### Open

If everything went right - you should be able to access Blipper web app at http://localhost:7070
