
# ADR 12: Use of Relational/Document Databases

- **Date created**: 20/01/2023
- **Driver**: Lee Measures (Not Foxy)

## Status

![proposed]

## Context

Determining which type of Database to use in the application and it's microservices (Relational/Document)

## Advice

Given the intended modular nature of the solution, I would recommend the usage of _both_ Relational [https://aws.amazon.com/relational-database/] and Document [https://www.mongodb.com/document-databases] databases, depending on the context that the database is going to be used in. 

For instance: The 'Core' of the application will be a series of _large_ datasets with a lot of relations, this suits a Relational database as it allows for more control over the selected information and how it is tied together, and is generally great for generating automated reports and data exports.

_However_ in the scenario where one of the microservices has a relatively small dataset that can be stored in a single Relational Database table, and there is no need for additional tables then a Document Database is much more suitable as it is faster to access and write to, in small chunks.

Hence, my recommendation for both to be used in conjunction with one another- but in separate use-cases. Additional information is available in the "Recommended Database Guidance.pdf" document provided separately.

## Decision

Develop databases using either Relational or Document database depending on the scope of the individual microservice it is being developed for

## Consequences

- Tailored databases developed on an as-needs basis to suit the context of development
- Larger datasets with ingrained relations can be split into smaller tables with implied relationships, allowing for easier contextual data access and exporting
- Smaller datasets stored as json allowing for rapid read/write access and less resource usage

[proposed]: https://img.shields.io/badge/Proposed-yellow?style=for-the-badge
[accepted]: https://img.shields.io/badge/Accepted-green?style=for-the-badge
[superceded]: https://img.shields.io/badge/Superceded-orange?style=for-the-badge
[rejected]: https://img.shields.io/badge/Rejected-red?style=for-the-badge
[deprecated]: https://img.shields.io/badge/Deprecated-grey?style=for-the-badge
