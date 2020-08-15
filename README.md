# Microservice API

* Sample Comment API using NodeJs, MongoDB (Docker), Azure Cognitive Service, Akismet. 

## Features
* XSS Protection (via [sanitize-html](https://www.npmjs.com/package/sanitize-html))
* Flags Spam (via [Akismet](https://akismet.com/))
* Flags rude or inappropriate language (English only via [Content Moderator](https://contentmoderator.cognitive.microsoft.com))
* Flags personally identifiable information (English only via [Content Moderator](https://contentmoderator.cognitive.microsoft.com))

## Running Locally

#### Prerequisites
* [Git](https://git-scm.com/downloads)
* [Node JS](https://nodejs.org/en/)
* [Mongo DB](https://www.mongodb.com)
* [Azure Content Moderator account (free)](https://contentmoderator.cognitive.microsoft.com)
* [Akismet Developer account (free)](https://akismet.com/development/api/#getting-started)

#### MongoDB Docker Compose

```bash
$ docker pull mongo:latest
```

#### Execution

##### Run Docker Compose File

```bash
$ docker-compose up
```

##### Run Docker Compose File in Background

```bash
$ docker-compose up -d
```

##### Login to container

```bash
$ docker exec -it avi_mongodb bash
```

#### 1. Install dependencies

```bash
$ npm i
```

#### 2. Modify the .env file
Save `dotenv` as `.env` and then add your database and Content Moderator + Akismet API details.

#### 3. Startup your MongoDB
Usually this is just: `mongod` on the command line.

#### 4. Start the server
To run in production mode where code is transpiled by Babel into a `dist` folder and run directly in `node`:

```bash
$ npm start
```

> To run in development mode where code is run by [babel-node](https://babeljs.io/docs/en/babel-node) via [nodemon](https://nodemon.io) and re-transpiled any time there is a change:

```bash
$ npm run dev
```

## Credits

* [Comments API](https://github.com/dev-mastery/comments-api)