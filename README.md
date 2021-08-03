<p align="center">
  <img src="logo.png" width="320" alt="Norik" />
</p>
  
  <p align="center">This is the backend part for getting to know NestJS during Norik internship.</p>

## Description

Use this boilerplate with Authentication & User module to work on assigned tasks during internship.

## Installation

```bash
$ npm install
```
## Running the app
Before running the app, docker-compose up command should executed to set up database & all other services (redis).
```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Migrations

```bash
# generate new migration
$ npm run typeorm migration:generate -- -n <migration_name>

# show migrations
$ npm run typeorm migration:show

# run migrations
$ npm run typeorm migration:run

# revert latest executed migration
$ npm run typeorm migration:revert
```

## Seeds

Currently docker-compose try to mount all the files from /seed/files into bucket named seed. When seeds are run images from this bucket are downloaded and uploaded via MediaService to desired bucket (original + compressed). SO make sure you have all of the images inside the folder. This folder is ignored by .gitignore and by .dockerignore.
To run seeds simply run

```bash
# run seeds
$ npm run seed
```

## Develop

Here are some guidlines for developers.

### New module

When you want to add new module with controller and service, always do it by using NestJS internal commands.

```bash
# Create new module
$ nest g module NewModule

# Create new controller
$ nest g controller NewModule

# Create new service
$ nest g service NewModule
```
### Source control guidelines

Feature branches are used to develop new features for the upcoming future release. When starting development of a feature the branch is always created from the develop branch. The essence of a feature branch is that it exists as long as the feature is in development and is merged back into develop branch when the feature is completed.
Example of naming: feature/email-login

## Authors

- [Martin Kozmelj](https://www.linkedin.com/in/martinkozmelj/)
- [Jaka Purg](https://www.linkedin.com/in/jaka-purg-9b25551a6/)