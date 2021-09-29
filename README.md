# Node.js Weight Tracker

![Demo](docs/build-weight-tracker-app-demo.gif)

This sample application demonstrates the following technologies.

* [hapi](https://hapi.dev) - a wonderful Node.js application framework
* [PostgreSQL](https://www.postgresql.org/) - a popular relational database
* [Postgres](https://github.com/porsager/postgres) - a new PostgreSQL client for Node.js
* [Vue.js](https://vuejs.org/) - a popular front-end library
* [Bulma](https://bulma.io/) - a great CSS framework based on Flexbox
* [EJS](https://ejs.co/) - a great template library for server-side HTML templates

**Requirements:**

* [Node.js](https://nodejs.org/) 12.x or higher
* [PostgreSQL](https://www.postgresql.org/) (can be installed locally using Docker)
* [Free Okta developer account](https://developer.okta.com/) for account registration, login

## Install and Configuration

1. Clone or download source files
1. Run `npm install` to install dependencies
1. If you don't already have PostgreSQL, set up using Docker
1. Create a [free Okta developer account](https://developer.okta.com/) and add a web application for this app
1. Copy `.env.sample` to `.env` and change the `OKTA_*` values to your application
1. Initialize the PostgreSQL database by running `npm run initdb`
1. Run `npm run dev` to start Node.js

The associated blog post goes into more detail on how to set up PostgreSQL with Docker and how to configure your Okta account.



## Emphasis:
app-
* nodejs 14v
* in .env file edit pghost, pgpassword, ip address, and your okta configuration
* in src/index.js edit ip address


postgress-
* configure pass to postgres user after installation
* pg.hba.conf add " host all all {IP}/32 trust"
* postgresql.conf add " listen.addresses = '*' "

## env example:
### Postgres configuration
PGHOST=*the host ip address* </br>
PGUSERNAME=postgres </br>
PGDATABASE=postgres </br>
PGPASSWORD=*your password* </br>
PGPORT=5432 </br>
#Node Weight Tracker </br> 
HOST_URL=http://*your ip address*:8080/ </br> 
COOKIE_ENCRYPT_PWD=superAwesomePasswordStringThatIsAtLeast32CharactersLong! </br>
NODE_ENV=development </br>
### Okta configuration </br>
OKTA_ORG_URL=*your okta url* </br>
OKTA_CLIENT_ID=*your client id* </br>
OKTA_CLIENT_SECRET=*your client secret* </br>
