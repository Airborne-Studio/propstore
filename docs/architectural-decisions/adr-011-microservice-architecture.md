
# ADR 11: Use of a Microservice Architecture

- **Date created**: 20/01/2023
- **Driver**: Lee Measures (Not Foxy)

## Status

![proposed]

## Context

Choosing a suitable IaaS (Infrastructure as a Service) Service for use as a backend to the proposed solution

## Advice

I highly recommend implementing a Microservice Architecture [https://microservices.io/] over a Monolithic Architecture [https://www.techtarget.com/whatis/definition/monolithic-architecture]. Developing as microservices allows for a faster and more reliable deployment cycle, with significantly reduced downtime or lack of service to the end-user.

Using a Microservice Architecture allows for the development and deployment of a series of small modules that are loosely coupled such that if any one of the modules goes down for whatever reason it will have minimal effect on the efficacy of the other modules.

Microservices can also be enabled/disabled as needed, such that if a future development supercedes an older module, the old one can be disabled without the need to fully redeploy the entire application, you need only disable the old module and enable/deploy the new one to replace it.

The general intention with this recommendation is to encourage the customer's desire for a modular application where pieces of functionality can be 'tacked on' after the fact, making the solution as a whole significantly easier to maintain and much more scalable in it's capabilities.

## Decision

Develop the solution using a Microservice Architecture

## Consequences

- Encouraging an overall modular solution
- Services are independently deployable, preventing solution down-time during deployments
- Loosely coupled modules prevents overall solution down time in the event of a module malfunction.
- Rapid development cycles
- Encourages Single Source of Truth in data management

[proposed]: https://img.shields.io/badge/Proposed-yellow?style=for-the-badge
[accepted]: https://img.shields.io/badge/Accepted-green?style=for-the-badge
[superceded]: https://img.shields.io/badge/Superceded-orange?style=for-the-badge
[rejected]: https://img.shields.io/badge/Rejected-red?style=for-the-badge
[deprecated]: https://img.shields.io/badge/Deprecated-grey?style=for-the-badge
