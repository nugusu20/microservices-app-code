# Source Import Inventory

This document explains which application files were imported into this repository, where they came from, and why they are included.

## Source

The application source code is based on Docker's official example voting application:

https://github.com/dockersamples/example-voting-app

The imported application components are used as a learning base for a DevOps project focused on Docker, Kubernetes, Helm, CI, and GitOps.

## Imported Components

### vote/

Purpose:

Web service that allows users to submit votes.

Technology:

Python / Flask

Important files:

- app.py
- requirements.txt
- templates/
- static/
- Dockerfile

Why it is included:

This service represents the user-facing voting frontend.

---

### result/

Purpose:

Web service that displays the voting results.

Technology:

Node.js

Important files:

- server.js
- package.json
- package-lock.json
- views/
- tests/
- Dockerfile

Why it is included:

This service represents the result frontend that reads voting data from the database.

---

### worker/

Purpose:

Background service that processes votes.

Technology:

.NET / C#

Important files:

- Program.cs
- Worker.csproj
- Dockerfile

Why it is included:

This service demonstrates asynchronous processing between Redis and PostgreSQL.

## Not Imported as Application Code

Redis and PostgreSQL were not imported as source code because they are infrastructure services, not application code written for this project.

They will be defined later through Docker, Kubernetes, and Helm configuration.

## Files Added by This Project

- README.md
- ATTRIBUTION.md
- third_party/docker-example-voting-app-LICENSE
- docs/source-inventory.md

## Project Ownership Boundary

The application source is based on Docker's example application.

The DevOps implementation, repository structure, documentation, container workflow, Kubernetes deployment, Helm chart, CI pipeline, and GitOps workflow are built as part of this project.
