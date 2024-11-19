# Nest.js & Typescript clean-code - SOLID

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Installation

```bash
$ yarn install
```

## Running the app

```bash
# development
$ yarn run start

# watch mode
$ yarn run start:dev

# production mode
$ yarn run start:prod
```

## Test

```bash
# unit tests
$ yarn run test

# e2e tests
$ yarn run test:e2e

# test coverage
$ yarn run test:cov
```

## Create Project

### Rreate nestjs project

```bash
# Create the nestjs project
$ nest new nest-SOLID
# ? Which package manager would you ❤️  to use? yarn
$ cd nest-solid
$ code .
```

### Processes to create Prisma and DB
 - reference: [Prisma Schema](https://www.prisma.io/docs/concepts/components/prisma-schema), [Prisma CLI](https://www.prisma.io/docs/reference/api-reference/command-reference), [Seeding DB](https://www.prisma.io/docs/guides/migrate/seed-database)

```bash
# install prisma cli as dev dependency (in the project folder)
$ yarn add prisma --save-dev

# Initiate prisma to create schema.prisma in folder prisma
$ yarn prisma init

# The generate command generates assets like Prisma Client based on the generator and data model blocks defined in your prisma/schema.prisma file.
$ yarn prisma generate

# The db push command pushes the state of your Prisma schema file to the database without using migrations. It creates the database if the database does not exist.
$ yarn prisma db push
```

## SOLID principle

1. SRP - Single Responsibility Principle:
     - Aim to have each class or module responsible for a single task or functionality related to your e-commerce store. For example, you could have separate modules for handling product management, order processing, and user authentication.
     - Avoid creating God objects that try to handle mutiple responsibilities. Splite your code into smaller, focused modules that are easier to understand and maintain.
2. OCP - Open/Close Principle:
    - Design your code to be open for extension but closed for modification. THis means that when you need to add new features or modify existing behavior, you should do so by extending or creating new cleasses, rather than modifying the existing ones.
    - Use dependency injection (DI) in Nest.js to inject dependencies into your classes. This makes it easier to swap implementations and extend functionality without modifying the existing code.
3. LSP - Liskov Subsitutuion Principle:
    - Ensure that subclasses or derived cleases can be substituted for their base classes without affecting the correctness of the program.
    - Design your application's interfaces and contracts carefully to allow for polymorphism and interchangeable components.
4. ISP - Interface Segregation Principle:
    - Define fine-grained interfaces that are tailored to the specific needs of the consumers. Avoid creating large interfaces with unnecessary methods.
    - Split your interfaces into smaller, more focused ones, allowing clients to depend only on the interfaces they require.
5. DIP - Dependency Inversion Principle:
    - Depend on abstractions rather than concrete implemenatations. This allows for loose coupling between components and facilities easier testing and maintenance
    - Use interfaces or abstract classes to deine cintracts and rely on them in your code. Apply dependency injection to provide implementations of these contracts.


## Reference

- [Nest.js & Typescript clean-code - SOLID](https://www.youtube.com/watch?v=vE74gnv4VlY&list=TLPQMjgwMTIwMjQb_Md5tOANBA&index=6)
