# FairTime

This is central repository for fair management system, it contains 2 submodules:
- fairs-api - api, written in Flask
- fairs-front - application front end, written in Vue.js


## How to run

1. Clone submodules
    ```bash
    $ git submodule init
    $ git submodule update
    ```
1. First run
    ```bash
    $ docker-compose build # builds api image
    $ docker-compose run -it backend flask --app=fairs_api db upgrade # create database
    $ docker-compose run -it backend flask --app=fairs_api seed # fill database
    $ docker-compose up # first run will fail, run this command again
    ```
1. Next runs
    ```bash
    $ docker-compose up
    ```

Open [webpage](http://localhost)
