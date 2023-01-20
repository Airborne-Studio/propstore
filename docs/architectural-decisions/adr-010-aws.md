
# ADR 10: Use of AWS IaaS as a backend

- **Date created**: 20/01/2023
- **Driver**: Lee Measures (Not Foxy)

## Status

![proposed]

## Context

Choosing a suitable IaaS (Infrastructure as a Service) Service for use as a backend to the proposed solution

## Advice

I recommend using AWS [https://aws.amazon.com/] as your IaaS over Azure [https://azure.microsoft.com/en-gb]. AWS is a more well rounded and intuitive solution to cloud hosted infrastructure.

AWS and Azure provide many of the same services, albiet with differing experiences in setup and configurability.

AWS provides a much more intuitive user experience in terms of budgetting costs, navigating modules and services.

AWS allows for automated scaling of resources with a kind of 'pay as you go' cost management system. (i.e. If usage goes down, services can be configured to automatically turn off and costs go down, if usage goes up, services spin up again to prevent any loss of service to the end user, and costs go up).

Using third party tools like Docker [https://www.docker.com/] and Terraform [https://www.terraform.io/] is generally much simpler to implement with AWS over Azure


## Decision

Implement AWS as the Cloud Hosted IaaS Service for the proposed solution

## Consequences

- Improved cost management and budgetting
- More intuitive development
	- Reduced development costs
	- Less complex documentation required
- Superior Scalability 
	- Cost effective scalability
	- Configured to have only as many resources active as is necessary for the site to remain active based on usage.
- Deployments with Docker&Terraform are simpler to implement
- Single hosting solution for Databases, APIs, Backend-Functions, and the Frontend UI

[proposed]: https://img.shields.io/badge/Proposed-yellow?style=for-the-badge
[accepted]: https://img.shields.io/badge/Accepted-green?style=for-the-badge
[superceded]: https://img.shields.io/badge/Superceded-orange?style=for-the-badge
[rejected]: https://img.shields.io/badge/Rejected-red?style=for-the-badge
[deprecated]: https://img.shields.io/badge/Deprecated-grey?style=for-the-badge
