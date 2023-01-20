# ADR 9: Use Formik for form management

- **Date created**: 15/01/2023
- **Driver**: Alex Foxleigh (Foxy)

## Status

![proposed]

## Context

A form is a common element in web applications. It is a way for users to input data into the application. The data can then be used to perform some action, e.g. create a new user, update a user, create a new post, update a post, etc. However forms are notoriously difficult to get right. There are a number of common issues that can occur when building forms:

- Validation
- Error handling
- Accessibility
- Performance
- State management

Formik solves many (but not all) of these problems. It is a library that provides a set of tools to help you build forms in React. It is a popular library with over 100,000 weekly downloads on NPM. It is also well maintained with regular updates and bug fixes.

Out of the box, Formik provides devlopers with two options:

- `Formik` - Formik itself is effectively a small library of components with a wrapper around the React Context API. It provides a number of useful features such as validation, error handling, accessibility and performance.
- `useFormik` - This is a hook that provides the same functionality as `Formik` but in a hook format. This is useful if you want to use Formik in a custom component.

I have personally only ever used `useFormik` as I prefer to use hooks in my own components. However, the learning curve for Formik will be lower if you use `Formik` the way they originally intended it to be used. Which is as a library of form components.

## Advice

I recommend using Formik to manage forms in the application. I recommend using `useFormik` as it is more flexible and allows you to use Formik in your own components which I personally believe would add more flexibility to the project. However, you will definitely save some time and have an easier time onboarding new developers if you use `Formik` as a library of form components as the documentation is much more comprehensive and easier to follow.

I would also recommend using the `yup` library for validation. This is a popular validation library that is well maintained and has a large community of developers. It is also very easy to use and has a very similar API to Formik. This solves the 'validation' problem in a much more elegant way than Formik does.

## Discussions

- Alex Foxleigh - This is the place to discuss the ADR. Please keep the discussion
  on topic and try to avoid repeating the same points. Please put your name next to
  any points you make.

## Decision

Implement Formik into the application.

## Consequences

- Formik is a popular library with over 100,000 weekly downloads on NPM. This means that there is a large community of developers who are familiar with the library and can help with any issues you may have.
- Form components are already built into the library. This means that you can get up and running with forms very quickly.
- Form state is managed by Formik (and integrates well into Redux) and can be accessed by any component in the application. This means that you can easily access form state from anywhere in the application.
- Formik is well maintained and has regular updates and bug fixes, which means that you can be confident that the library will continue to be supported for the foreseeable future.

[proposed]: https://img.shields.io/badge/Proposed-yellow?style=for-the-badge
[accepted]: https://img.shields.io/badge/Accepted-green?style=for-the-badge
[superceded]: https://img.shields.io/badge/Superceded-orange?style=for-the-badge
[rejected]: https://img.shields.io/badge/Rejected-red?style=for-the-badge
[deprecated]: https://img.shields.io/badge/Deprecated-grey?style=for-the-badge
