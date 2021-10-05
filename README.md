# enstars-dev
Dev environment for enstars.info

1. Clone this repo where you want your development enviornment to live, everything will be run from this directory

    `git clone https://github.com/ceec/enstars-dev.git`

2. Go into the directory where you cloned the repo and run

    `docker-compose up -d --build enstars`

    This will bring up the containers for the development environment.

3. Navigate to `http://localhost:9876/` to see the site.

    If you want to use a different port it is set up on line 13 of docker-compose.yml