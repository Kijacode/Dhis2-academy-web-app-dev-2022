# Final Project: Build a DHIS2 application

This project will focus on what you've learned during **Workshop 1 and 2** and you will take that knowledge to build a DHIS2 application. 🎊

Successful completion of this project and attendance in Workshop 2 are the prerequisites to earn a **DHIS2 Completion certificate** for this Academy program.

> **Note:** For participants that have submitted Project 1, feel free to expand on the same project to build this Final Project and include the tools that you've learned in Workshop 2.

## Description

In this project you are going to be making a React application that uses the DHIS2 API to retrieve and send data to a DHIS2 instance using queries and mutations you have defined with the help of the DHIS2 Application Runtime.

You are free to choose the purpose of your application in this project. We only require that the requirements below be followed.

## Requirements

- **Must** be [initiatialized with the DHIS2 Application
  Platform](../../workshop-1/01-environment-setup/README.md)
- **Must** use a layout with sidebar navigation. See [example](../../workshop-1/02-ui-library/README.md) from the UI-library exercise in Workshop 1.
- **Must** use [React Router](https://reactrouter.com/web/guides/quick-start) for routing and contain at least two unique routes with route relevant components and data
- [`@dhis2/ui`](https://ui.dhis2.nu/demo/) components **must**
  be used to build custom forms, tables and components wherever applicable
- App **must** contain at least one component that uses a [data query](https://runtime.dhis2.nu/#/hooks/useDataQuery) (`useDataQuery` hook) _AND_ at least one component that uses a [mutation](https://runtime.dhis2.nu/#/hooks/useDataMutation) (`useDataMutation` hook) from the DHIS2 Application Runtime (using dynamic queries and variables)
- App **must** use the `useAlert` hook to show alerts. See [example](https://github.com/dhis2/academy-web-app-dev-2022/tree/main/workshop-2/01-advanced-app-runtime/exercises-solution) from the App Runtime exercises.
- Remember to take into account [performance and security best practices](https://github.com/dhis2/academy-web-app-dev-2022/tree/main/workshop-2/03-performance-security)
- **BONUS:** You are more welcome to include any of the tools that you've learned during these workshops!

## Deadline

#### **June 15, 2022**

## Submission details

1. Join GitHub Classroom through this [link](https://classroom.github.com/a/EQw8Kv6H).
2. Follow these [instructions](../../resources/GET_STARTED.md) on how to get started with Github Classroom
3. Feel free to create your application in this directory `final-project`
4. Submit your project to Github Classroom

We look forward to seeing your project! 😬
