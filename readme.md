# Usage
## Server Deployment Project

Two proyects deployed at AWS(Amazon Web Services) using Nginx
 
`NodeJs:` http://ec2-44-211-140-248.compute-1.amazonaws.com/

`React:`  http://44.211.140.248/

## First step, set your enviroment

1. Download and install `Node` from `https://nodejs.org/`
2. Download and install `MongoDB` from `https://www.mongodb.com/`
3. Copy `.env.example` into `.env` and set your own config

## Install Dependencies

    npm install

## First time

    npm run setup

Installs dependencies, runs `build` to generate Babel's compilation, runs `initDB` to setup DB and runs `npm start` to start development

## Set Initial DB

    npm run initDB

Drops Adverts DB and loads placeholder data from `initialAdverts.json`

## Dev Start

    npm start

---

![image](https://user-images.githubusercontent.com/103906418/206923543-92b9a955-5812-4c67-a9e6-40a1465632f9.png)


## API Routes

## `You will need to use `Postman` or any other similar platforms.`

# For login the only credential that are accepted are:

    user : admin@example.com password : 1234
    user : user@example.com password : 1234

## GET

    /api/adverts

Returns all the adverts

    /api/adverts/?someFilters

Returns a filtered list. Admits filter by fields, sorting, skipping and limit reuslts. E.g:

` /api/adverts/?select=name price -_id&name=BikeBans&sort=-name price`

## POST

    /api/register

Returns a JWT needed to access all other API routes

    /api/adverts

Create a new advert

    /api/thumbnail

Returns an URL with the 100x100 thumbnail of the given image

## PUT

    /api/adverts/id

Updates the match ID element

## DELETE

    /api/adverts/id

Deletes the match ID element

