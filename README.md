# Workspace

This project was generated using [Nx](https://nx.dev).

This is the resultant of following the article — [Tiny Angular application projects in Nx workspaces](https://indepth.dev/tiny-angular-application-projects-in-nx-workspaces/) —


> We have generated an Nx workspace with a single Angular application. Even before adding any features, we can extract workspace libraries to adhere to the Single Responsibility Principle.

>## The assets library
>The shared assets workspace library contains static files such as web fonts, icons, and images. It also contains the favicon. The web app manifest would also be added here.

>We saw an example of adding an image file to this library and referring to it from our application project. Of course, this works from UI workspace libraries and feature libraries as well.

>With static files located in a separate workspace library, we lower the risk of breaking the whole application when adding, deleting or modifying static files.

>## The styles library
>With a workspace library exclusively for global styles, we won't have to feel bad for polluting the application project with dozens of Sass partials or risk breaking the application setup by accident.

>The shared styles workspace library could also expose Sass mixins, functions, and partials that are shared between component styles or UI workspace libraries.

>## The environments library
>Extracting the environment files to a shared workspace library allows us to conditionally configure injectors from workspace libraries such as the shared data access library we created to configure NgRx Store in the root injector.

>In a real application, we could add a feature shell library so that it would become the orchestration Angular module imported by AppModule or CoreModule.

>Without a feature shell library, we have to make changes to the application project to add further configure the root injector or add application use cases. This is risky. We're better off leaving the application project untouched under most circumstances to have peace of mind.

>## Shared workspace libraries
>In the examples demonstrated in this article, we have put the extracted workspaces libraries in the shared library grouping folder and added the scope:shared tag. For workspaces with only a single application, this might not be necessary.

>However, as the application grows, we will be happy that we used grouping folders from the beginning of the project. Application-wide workspace libraries are in the shared grouping folder, while we use for example sub-domain grouping folders to group our feature libraries and their related data access, domain, and UI workspace libraries.

>Alternatively, we would end up with dozens if not hundreds of library folders within the libs folder, each with increasingly long folder names.

>If it turned out that we wanted to add additional applications to the workspace, we would keep the workspace libraries that we wanted to share between the applications in the shared library grouping folder. The ones that we could or would not want to share between the applications could be placed within a library grouping folder named after the application, for example libs/tiny-app/shared for application-wide libraries unique to the tiny-app application project.


🔎 **Nx is a set of Extensible Dev Tools for Monorepos.**

## Quick Start & Documentation

[Nx Documentation](https://nx.dev/angular)

[10-minute video showing all Nx features](https://nx.dev/angular/getting-started/what-is-nx)

[Interactive Tutorial](https://nx.dev/angular/tutorial/01-create-application)

## Adding capabilities to your workspace

Nx supports many plugins which add capabilities for developing different types of applications and different tools.

These capabilities include generating applications, libraries, etc as well as the devtools to test, and build projects as well.

Below are some plugins which you can add to your workspace:

- [Angular](https://angular.io)
  - `ng add @nrwl/angular`
- [React](https://reactjs.org)
  - `ng add @nrwl/react`
- Web (no framework frontends)
  - `ng add @nrwl/web`
- [Nest](https://nestjs.com)
  - `ng add @nrwl/nest`
- [Express](https://expressjs.com)
  - `ng add @nrwl/express`
- [Node](https://nodejs.org)
  - `ng add @nrwl/node`

## Generate an application

Run `ng g @nrwl/angular:app my-app` to generate an application.

> You can use any of the plugins above to generate applications as well.

When using Nx, you can create multiple applications and libraries in the same workspace.

## Generate a library

Run `ng g @nrwl/angular:lib my-lib` to generate a library.

> You can also use any of the plugins above to generate libraries as well.

Libraries are sharable across libraries and applications. They can be imported from `@workspace/mylib`.

## Development server

Run `ng serve my-app` for a dev server. Navigate to http://localhost:4200/. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng g component my-component --project=my-app` to generate a new component.

## Build

Run `ng build my-app` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test my-app` to execute the unit tests via [Jest](https://jestjs.io).

Run `nx affected:test` to execute the unit tests affected by a change.

## Running end-to-end tests

Run `ng e2e my-app` to execute the end-to-end tests via [Cypress](https://www.cypress.io).

Run `nx affected:e2e` to execute the end-to-end tests affected by a change.

## Understand your workspace

Run `nx dep-graph` to see a diagram of the dependencies of your projects.

## Further help

Visit the [Nx Documentation](https://nx.dev/angular) to learn more.
