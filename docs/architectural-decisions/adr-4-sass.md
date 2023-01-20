# ADR 4: Use SASS as our Theming engine

- **Date created**: 06/01/2023
- **Driver**: Alex Foxleigh (Foxy)

## Status

![proposed]

## Context

Choosing a suitable CSS stack for our theming engine.

## Advice

I recommend using [SASS](https://sass-lang.com/) over
[CSS-in-JS](https://cssinjs.org). SASS is a much more mature and powerful CSS engine than CSS-in-JS and when combined with (S)CSS-modules, it can be used to create a modular CSS system with all of the benefits of CSS-in-JS.

SASS also has a lot of powerful features that CSS-in-JS does not have, such as mixins, nesting and functions, which can be used to create a robust and comprehensive theming engine.

We would be specifically using the 'SCSS' syntax for SASS as this is more
closely aligned with the CSS specification.

## Alternatives

Another contender for this decision was [TailwindCSS](https://tailwindcss.com/). Whilst TailwindCSS is a very powerful CSS framework, it is not a CSS engine and does not have the same level of flexibility as SASS. It is also a much more opinionated framework and does not have the same level of customisability as SASS.

I would recommend against Tailwind as it is not as mature as SASS and also adds a lot of bloat to the project. It is also not as future-proof as SASS and will be harder to maintain in the long run.

## Discussions

- Alex Foxleigh - This is the place to discuss the ADR. Please keep the discussion
  on topic and try to avoid repeating the same points. Please put your name next to
  any points you make.

## Decision

Implement SCSS as our Theming engine.

## Consequences

- All components will be modular and reusable with standalone SCSS-modules
  whilst still having access to the variables, mixins and functions from the main theme.
- We will be adopting a robust and well supported CSS framework with a huge
  ecosystem of plugins and extensions. As well as a solid number of developers who will be able to work with this technology for years to come.
- Encourages separation of concerns and modularity.
- We will have a large community of developers who are willing to help with
  any issues we may have.
- Hiring and onboarding new developers will be easier as there is a large
  community of developers who are familiar with SASS.

[proposed]: https://img.shields.io/badge/Proposed-yellow?style=for-the-badge
[accepted]: https://img.shields.io/badge/Accepted-green?style=for-the-badge
[superceded]: https://img.shields.io/badge/Superceded-orange?style=for-the-badge
[rejected]: https://img.shields.io/badge/Rejected-red?style=for-the-badge
[deprecated]: https://img.shields.io/badge/Deprecated-grey?style=for-the-badge
