# Millefeuille Tech Stack

A quick run down of the proposed tech stack.

- [Ideal architecture](#Ideal-architecture)
- [Immediate architecture](#Immediate-architecture)
- [CI/CD using Google Code Build or CircleCI?](#CI/CD-using-Google-Code-Build-or-CircleCI?)
- [Why Firebase instead of PostgreSQL/Nodejs?](#Why-Firebase-instead-of-PostgreSQL/Nodejs?)
- [Monorepo](#Monorepo)
- [Domains and namespaces](#Domains-and-namespaces)


## Ideal architecture

The app will be split into various parts using a plugin architecture. The core app will essentially be a plugin runner while everything else will be a plugin. Each plugin should be standalone, with the core being its only dependency.

This design is so that it will be possible for users to self host their own instances and picking and choosing only the features they need. **How this will be achieved yet is uncertain.**

Server side functionality will essentially be wrapped in a docker container that users may self host. The client will be a standard web front end, with the core portions SSRed while non core functionality should be lazy loaded on demand.

A stand-alone desktop app built on Electron would be nice to have too.

Database will be PostgreSQL with maybe a redis or filesystem DB for market data. Load balancing can most probably be handled with Nginx.

## Immediate architecture

Firebase for user authentication and databases. Web based front end client built using React framework, charts rendered with D3. Main language will be Typescript.

Eslint and Prettier should use recommended rule sets.

## CI/CD using Google Cloud Build or CircleCI?

Let's use both. Maybe even Amazon's CodeBuild.

## Why Firebase instead of PostgreSQL/Nodejs?

So I can skip backend development and focus on frontend.

## Monorepo

Everything in a single git repo. It’ll probably not be necessary in the beginning, as functionality expands, we’ll probably have to introduce Lerna.

Using npm packages as an example,
- @millefeuille/core
- @millefeuille/Authenticator
- @millefeuille/ledger
- @millefeuille/marketWatch

## Domains and namespaces

Successfully registered [Millefeuille namespace](https://www.npmjs.com/org/millefeuille) at npm. GitHub name is already taken so we might need an alternative. Or maybe host it under the `thelegendofcode` org.

[millefeuille.app](millefeuille.app) and [millefeuille-app.com](millefeuille-app.com) domains successfully registered through google domains. Consider getting [mille-feuille.app](mille-feuille.app) too?
