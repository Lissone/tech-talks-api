<h1 align="center">
  TechTalks API
</h1>

<p align="center">
  <a href="#description">Description</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#requirements">Requirements</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#technologies">Technologies</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#usage">Usage</a>
</p>
<br />
<p align="center">
  <img src="https://img.shields.io/static/v1?label=license&message=MIT" alt="License">
  <img src="https://img.shields.io/github/repo-size/Lissone/tech-talks-api" alt="Repo size" />
  <img src="https://img.shields.io/github/languages/top/Lissone/tech-talks-api" alt="Top lang" />
  <img src="https://img.shields.io/github/stars/Lissone/tech-talks-api" alt="Stars repo" />
  <img src="https://img.shields.io/github/forks/Lissone/tech-talks-api" alt="Forks repo" />
  <img src="https://img.shields.io/github/issues-pr/Lissone/tech-talks-api" alt="Pull requests" >
  <img src="https://img.shields.io/github/last-commit/Lissone/tech-talks-api" alt="Last commit" />
</p>

<p align="center">
  <a href="https://github.com/Lissone/tech-talks-api/issues">Report bug</a>
  ·
  <a href="https://github.com/Lissone/tech-talks-api/issues">Request feature</a>
</p>

<br />

## Description

TechTalks is a discussion forum API focused on software technologies, where users can create topics, respond to questions, and share knowledge. This project was a great opportunity for me to dive deep into Domain-Driven Design (DDD) and build a clean, well-organized architecture with NestJs.

This project was special to me for several reasons. It was my first experience using Cloudflare for file uploads, which brought new challenges but also valuable learnings. Additionally, it was the first time I worked with such a complex and well-structured architecture, something that truly motivated me to continue exploring this approach in future projects.

I made sure to maintain highly tested and reliable code. With that in mind, I implemented a wide range of unit tests and end-to-end (E2E) tests, resulting in excellent test coverage that ensures the quality and robustness of the application.

## Requirements

- [Nodejs](https://nodejs.org/en/)
- [Npm](https://www.npmjs.com/)
- [Pnpm](https://pnpm.io/pt/)
- [Docker](https://www.docker.com/)

## Technologies

- Nodejs
- Typescript
- NestJs
- Prisma
- Postgresql
- Redis
- Cloudflare / AWS
- Zod
- FakerJs
- Vitest
- Supertest
- Eslint
  - @rockeseat/eslint-config
- Prettier

## Usage

You can clone it on your pc using the command:

```bash
git clone https://github.com/Lissone/tech-talks-api.git
cd tech-talks-api
```

### Add environment variables

```bash
# .\.env

# App
PORT=3333

# Jwt
JWT_PRIVATE_KEY=
JWT_PUBLIC_KEY=

# Database
DATABASE_URL="postgresql://docker:docker@localhost:5432/tech-talks?schema=public"

# Redis
REDIS_HOST="127.0.0.1"
REDIS_PORT=6379
REDIS_DB=0

# Cloudflare / AWS
CLOUDFLARE_ACCOUNT_ID=
AWS_BUCKET_NAME=tech-talks
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
```

### Install dependencies

```bash
pnpm install
#or
npm install
```

>  ❗  You must have **Docker installed** on your machine to get the container up.
**Up Postgresql and Redis services** in a **Docker container** on your local machine using:

```bash
docker-compose up -d
# View all running containers
docker ps
```

### Run migrations

You need to run a prisma script command to run all current migrations:

```bash
npx prisma migrate dev
```

### Run project

```bash
pnpm start:dev
#or
npm run start:dev
```

> ℹ️  You can **view the database** from Prisma Studio on the two services that use Prisma, using:

```bash
pnpm prisma-studio
#or
npm run prisma-studio
```

## License

Distributed under the MIT License. See `LICENSE` for more information.

<h4 align="center">
  Made with ❤️ by <a href="https://github.com/Lissone" target="_blank">Lissone</a>
</h4>

<hr />