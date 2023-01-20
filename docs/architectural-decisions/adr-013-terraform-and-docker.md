
# ADR 13: Using Terraform & Docker for Automated Deployments

- **Date created**: 20/01/2023
- **Driver**: Lee Measures (Not Foxy)

## Status

![proposed]

## Context

Deciding if deployments should be automated or manual, and if automated what technologies to use.

## Advice

I would highly recommend automated deployments, it reduces the legwork of the development team and drastically reduces the potential for human-error. Following on from this, there are two technologies that, when used in tandem, would be a perfect fit for the proposed solution: Terraform [https://www.terraform.io/] and Docker [https://www.docker.com/].

Terraform provides the dev team with the ability to define the entire infrastructure of the solution, down the the approvals required for deployments, using code. This code is kept in a repository along with the rest of the solution and thus allows for version control over the infrastructure of the solution- further reducing the risk of human error.

Docker allows for the containerisation of applications, and therefore microservices- allowing them to spin up or down as needed without affecting any other containers.

These two technologies operating in tandem allow for a rapid deployment cycle that is automated from Pull-Request to Deployment, alongside allowing local dev environments to be spun up that are effectively identical simulations of the production and dev-test environments which greatly improves the speed and quality of the development team, along-side allowing for a greater reliability in testing, further reducing human error risks and providing greater confidence in the proposed solution.

## Decision

Implement and Document solution architecture in Terraform, combining with Docker to provide a containerised solution with automated deployments

## Consequences

- Highly scalable solution infrastructure
- Reduction in maintenance overhead for infrastructure and deployments
- Automated microservice deployments
- Local development environments a 1:1 simulation of live environments
  - Improved development speed and reliability
  - Greater confidence in solution efficacy
  - Improved testability
 

[proposed]: https://img.shields.io/badge/Proposed-yellow?style=for-the-badge
[accepted]: https://img.shields.io/badge/Accepted-green?style=for-the-badge
[superceded]: https://img.shields.io/badge/Superceded-orange?style=for-the-badge
[rejected]: https://img.shields.io/badge/Rejected-red?style=for-the-badge
[deprecated]: https://img.shields.io/badge/Deprecated-grey?style=for-the-badge
