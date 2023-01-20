# ADR 5: Use Builda as our repository manager

- **Date created**: 06/01/2023
- **Driver**: Alex Foxleigh (Foxy)

## Status

![proposed]

## Context

Making the repository easy to use and maintain is a key part of the project. We need to decide on a repository manager that will allow us to easily manage our packages and dependencies.

## Advice

I would recommend my own package, [Builda](https://builda.app/) is a application generation and repository managment tool. It allows you to create an application with a single command and then add elements to it with another command.

It would also allow for a centralised 'template app' that can then easily be reused for all microservices and even new projects which use the same stack. This centralised template app would be able to be updated with a single command and would then be able to be used to update all other microservices easily.

If repositories are hosted on a system with limited storage, Builda will dramatically reduce the amount of storage required as it will only store the files that have changed within that project.

## Discussions

- Alex Foxleigh - This is the place to discuss the ADR. Please keep the discussion
  on topic and try to avoid repeating the same points. Please put your name next to
  any points you make.

## Decision

Implement Builda as our repository manager.

## Consequences

- There will be a single template app that can be used to create new projects and microservices with a single command.
- All microservices and projects will be able to be synchronised with the template app with a single command, allowing for easy updates.
- Repositories will be much smaller as only the files that are unique to that project/microservice will be stored.
- Maintaining a coding standard will be easier as new components and pages do not need to be created from scratch.
- Builda is a new project and is still in development. This means that there may be some bugs and issues that need to be ironed out.
- Builda is brand new and therefore is not yet well known. This issue is mitigated by the fact that you know the devloper (me) and I will be more than happy to help with any issues you may have.

[proposed]: https://img.shields.io/badge/Proposed-yellow?style=for-the-badge
[accepted]: https://img.shields.io/badge/Accepted-green?style=for-the-badge
[superceded]: https://img.shields.io/badge/Superceded-orange?style=for-the-badge
[rejected]: https://img.shields.io/badge/Rejected-red?style=for-the-badge
[deprecated]: https://img.shields.io/badge/Deprecated-grey?style=for-the-badge
