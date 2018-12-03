## Running and development

1. Clone the repository
1. Run `npm install`
1. Run `docker-compose up` to start up the needed services (development database etc.)
1. Run `npm start`

The app is automatically started in watch mode, i.e. it recompiles whenever there's a change to a source file.

## Design principles

The 5 [SOLID](https://en.wikipedia.org/wiki/SOLID) principles.

**Dependency injection** with [`InversifyJS`](https://github.com/inversify/InversifyJS)

[Layered architecture](https://docs.microsoft.com/en-us/previous-versions/msp-n-p/ee658117(v=pandp.10)#LayeredStyle)
  - [`routing-controllers`](https://github.com/typestack/routing-controllers)
  - Separate service layer for business logic
  - Separate repository layer with [`knex`](http://knexjs.org/) + [`Objection`](https://vincit.github.io/objection.js/)

Integration layer utilizing the [Gateway pattern](https://martinfowler.com/eaaCatalog/gateway.html)