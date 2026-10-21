# Cloud Config

Configuration files served by the [config-server](https://github.com/danishahm89/config-server) to the microservices of this practice project.

All values are sample settings for local development. Databases are in-memory H2 with default development logins. This repository contains no real credentials.

## Files

| File | Service | Port |
|---|---|---|
| `account-management.yml` | account-management | 8081 |
| `customer-management.yml` | customer-management | see file |

Each file configures the service name, an in-memory H2 datasource, JPA and Hibernate settings, SQL initialization and the H2 console.

## How it is used

1. The Config Server clones this repository on start-up.
2. A microservice asks the Config Server for its configuration using its application name.
3. The Config Server returns the matching `{application-name}.yml` file.

## Related repositories

- [config-server](https://github.com/danishahm89/config-server)
- [eureka-server](https://github.com/danishahm89/eureka-server)
- [api-gateway](https://github.com/danishahm89/api-gateway)
