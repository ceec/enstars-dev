# enstars-dev
Dev environment for enstars.info

1. Clone this repo where you want your development enviornment to live, everything will be run from this directory

    `git clone https://github.com/ceec/enstars-dev.git`

2. Go into the directory where you cloned the repo and run

    `docker-compose up -d --build enstars`

    This will bring up the containers for the development environment.

3. Create a /src directory and clone the main enstars repo into it.

    `mkdir src`

    `cd src`

    `git clone https://github.com/ceec/enstars.git .`

    It is expecting src to have all the files so make sure the structure isn't src/enstars/

4. In the /src directory, create the vendor directory by running `docker-compose run --rm composer update`

5. Enstars.info uses Laravel as a framework which uses a .env file to control app settings

    1. In the /src directory, make a copy of `.env.example` named `.env`

    2. Generate an API key for `.env` by running `docker-compose run --rm artisan key:generate`

5. Navigate to `http://localhost:9876/` to see the site.

    If you want to use a different port it is set up on line 13 of `docker-compose.yml`