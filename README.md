# FairTime

This is central repository for fair management system, it contains 2 submodules:
- fairs-api - api, written in Flask
- fairs-front - application front end, written in Vue.js


## How to run

At this moment you have to have node installed locally to build front end files,
rest can be run with docker. 

1. Build front end assets.
    ```bash
    $ npm install
    $ npm run dev
    ```
1. First run
    ```bash
    $ docker-compose build # builds api image
    $ docker-compose run -it backend flask --app=fairs_api db upgrade # create database
    $ docker-compose run -it backend flask --app=fairs_api seed # fill database
    $ docker-compose up # start whole application
    ```
1. Next runs
    ```bash
    $ docker-compose up
    ```

