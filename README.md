Replace all `ToDo` notes in this file and adjust also the following files:
- package.json:
    - Adjust the general parts like name, description, ...
    - Adjust the scripts `npm run start`, `npm run build`, `npm run lint` and
      `npm run test` or change them if you use `yarn` for instance
- wcs-manifest.json:
    - Adjust the general parts like title, description, ...
    - Adjust the configuration part with all possible configuration options
      (https://webcomponents.opendatahub.bz.it/getting-started) and test them with the [Validator](https://webcomponents.opendatahub.bz.it/validator/)

# Webcomponent Covid Announcements

[![REUSE status](https://api.reuse.software/badge/github.com/noi-techpark/webcomp-boilerplate)](https://api.reuse.software/info/github.com/noi-techpark/webcomp-boilerplate)

This Webcomponent shows all data from Opendatahub Article Endpoint of type SpecialAnnouncement. Currently there are shown the latest Covid Announcements for entry to Italy, South Tyrol. General Covid rules in the skiareas etc..

## Table of contents

- [Usage](#usage)
- [Gettings started](#getting-started)
- [Tests and linting](#tests-and-linting)
- [Deployment](#deployment)
- [Docker environment](#docker-environment)
- [Information](#information)

## Usage

ToDo: Include the webcompscript file `dist/js/widget.js` in your HTML and define the web component like this:

```html
 <odh-covid-widget data-color="#333" data-lang="de" data-ignore="['85B7E735-CAD8-CFFD-CFE8-D5019469B322', '47915EAE-8631-4CBF-42D3-070677AAA366']"></odh-covid-widget>
```

### Attributes

#### data-color

Color of the Sliderarrows.

Type: string


#### data-lang

Widget Language.

Type: string
Options: "de", "it", "en"

#### data-ignore

hide Articles with id.

Type: string (Array at example "['85B7E735-CAD8-CFFD-CFE8-D5019469B322', '47915EAE-8631-4CBF-42D3-070677AAA366']")

## Getting started

These instructions will get you a copy of the project up and running
on your local machine for development and testing purposes.

### Prerequisites

To build the project, the following prerequisites must be met:

- ToDo: Check the prerequisites
- Node 12 / NPM 6

For a ready to use Docker environment with all prerequisites already installed and prepared, you can check out the [Docker environment](#docker-environment) section.

### Source code

Get a copy of the repository:

```bash
ToDo: git clone https://github.com/noi-techpark/webcomp-specialannouncement.git
```

Change directory:

```bash
ToDo: cd webcomp-specialannouncement/
```

### Dependencies

Download all dependencies:

```bash
npm install
```

### Build

Build and start the project:

```bash
npm run start:dev
```

The application will be served and can be accessed at [http://localhost:9000](http://localhost:9000).

## Tests and linting

The tests and the linting can be executed with the following commands:

```bash
npm run test
npm run lint
```

Currently there are no tests available.

## Deployment

To create the distributable files, execute the following command:

```bash
npm run build
```

## Docker environment

For the project a Docker environment is already prepared and ready to use with all necessary prerequisites.

These Docker containers are the same as used by the continuous integration servers.

### Installation

Install [Docker](https://docs.docker.com/install/) (with Docker Compose) locally on your machine.

### Dependenices

First, install all dependencies:

```bash
docker-compose run --rm app /bin/bash -c "npm install"
```

### Start and stop the containers

Before start working you have to start the Docker containers:

```
docker-compose up --build --detach
```

After finished working you can stop the Docker containers:

```
docker-compose stop
```

### Running commands inside the container

When the containers are running, you can execute any command inside the environment. Just replace the dots `...` in the following example with the command you wish to execute:

```bash
docker-compose run --rm app /bin/bash -c "..."
```

Some examples are:

```bash
docker-compose run --rm app /bin/bash -c "npm run test"
```

## Information

### Support

For support, please contact [help@opendatahub.bz.it](mailto:help@opendatahub.bz.it).

### Contributing

If you'd like to contribute, please follow the following instructions:

- Fork the repository.

- Checkout a topic branch from the `development` branch.

- Make sure the tests are passing.

- Create a pull request against the `development` branch.

A more detailed description can be found here: [https://github.com/noi-techpark/documentation/blob/master/contributors.md](https://github.com/noi-techpark/documentation/blob/master/contributors.md).

### Documentation

More documentation can be found at [https://opendatahub.readthedocs.io/en/latest/index.html](https://opendatahub.readthedocs.io/en/latest/index.html).

### Boilerplate

The project uses this boilerplate: [https://github.com/noi-techpark/webcomp-boilerplate](https://github.com/noi-techpark/webcomp-boilerplate).

### License

The code in this project is licensed under the GNU AFFERO GENERAL PUBLIC LICENSE Version 3 license. See the [LICENSE.md](LICENSE.md) file for more information.