# App

GymPass style app

This is the backend of a workout scheduling platform, where users can check in at gyms registered within a 100-meter radius of their current location.

## 🔑 Environment Variables

Before running the project, you need to configure the environment variables.

1. Create a file called `.env` and paste all the variables from `.env.example`
2. Make sure all variables are correctly set inside the `.env` file.

## 📦 Technologies

- [Node](https://nodejs.org/pt)
- [Fastify](https://fastify.dev/) - Fast and low-overhead web framework for Node.js
- [Zod](https://zod.dev/) - for schema validation
- [Prisma](https://www.prisma.io/) - for database interaction and ORM
- [Docker](https://www.docker.com/) - running the database in containers
- [Postgres](https://www.postgresql.org/) - relational database
- [Cypress](https://vitest.dev/) - for E2E testing
- [Vitest](https://vitest.dev/) - for unit testing

## 🚀 Installation and Running

Clone the repository:

```bash
git clone https://github.com/Rener-cardoso/03-api-solid.git
```

This project depends on Docker to setup database. With Docker installed, install dependencies, setup Docker containers and run the application:

```bash
npm install
docker compose up -d
npx prisma migrate dev
```

Start the project:

```bash
npm run dev
```

Open your browser at: [http://localhost:3333](http://localhost:3333)

## RFs (Functional Requirements)

- [x] User should be able to register;
- [x] User should be able to authenticate;
- [x] User should be able to view their profile;
- [x] User should be able to view the number of check-ins they have made;
- [x] User should be able to view their check-in history;
- [x] User should be able to search for nearby gyms (up to 10km);
- [x] User should be able to search for gyms by name;
- [x] User should be able to check in at a gym;
- [x] User check-in should be validated;
- [x] Admin should be able to register a gym;

## RNs (Business Rules)

- [x] User should not be able to register with a duplicate email;
- [x] User should not be able to check in twice on the same day;
- [x] User should not be able to check in unless within 100m of the gym;
- [x] Check-in can only be validated within 20 minutes after creation;
- [x] Check-in can only be validated by administrators;
- [x] Gyms can only be registered by administrators;

## RNFs (Non-Functional Requirements)

- [x] User passwords must be encrypted;
- [x] Application data must be persisted in a PostgreSQL database;
- [x] All data lists must be paginated with 20 items per page;
- [x] User should be identified by a JWT (JSON Web Token);
