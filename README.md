# MobileSpectrum

MobileSpectrum is OpenSource website showing many different contries mobile spectrum allocations. 

## Environments

Production: https://mobilespectrum.org

## Build and Deploy to production

Install Docker: https://docs.docker.com/get-docker/

Clone Repository

```
git clone https://github.com/olkitu/Mobilespectrum.git
```

### Docker

Use Docker and Docker Compose to set up production enviroment.

```
docker build -t olkitu/mobilespectrum .
```

The site will available on port 4000.

### Without Docker

Requirements:

* NodeJS 16.13
* Angular CLI
* Yarn

Use yarn to build Node modules and build to production

```
yarn
ng build --configuration production
```

And copy static `dist/MobileSpectrum` to webserver root directory. 

## Development

We recommend use Gitpod to setup development enviroment. You can also install it to locally.

Full Documentation: https://docs.mobilespectrum.org/

### Gitpod

Just click below to start development in Gitpod. You must register to service with your Gitlab account. 

[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/olkitu/Mobilespectrum)

### Docker

Build, install Node-modules and start dev environment. The first setup will take time because node_modules will be installed to persistent volume.

```
docker-compose build
docker-compose up -d
```

You can then modify files locally and see changes via browser http://localhost:4200

If you like to reinstall node_modules, stop Docker with `-v` parameter to remove persistent volume.

```
docker-compose down -v
```

### NodeJS locally

Requirements:

* NodeJS 16.13
* Angular CLI
* Yarn

Run `yarn` to install Node-modules

#### Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

#### Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

#### Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

#### Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

### Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
