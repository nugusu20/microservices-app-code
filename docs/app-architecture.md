# Application Architecture

This repository contains three application services from the voting application:

- vote
- worker
- result

Redis and PostgreSQL are required runtime services, but they are not application source code in this repository.

## Runtime Flow

```text
User
  |
  v
vote
  |
  v
Redis
  |
  v
worker
  |
  v
PostgreSQL
  |
  v
result
  |
  v
User
