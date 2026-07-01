# Microservices App Code

This repository contains the application source code for the DevOps Voting GitOps Lab.

## Application Components

- vote: web service for submitting votes
- result: web service for displaying voting results
- worker: background service that processes votes
- redis: queue used between vote and worker
- postgres: database used to store results

## Purpose

This project demonstrates a simple microservices architecture that will later be containerized with Docker, deployed to Kubernetes, and managed with GitOps.

## Local Docker Runtime

The application can be run locally with Docker Compose.

Runtime services:

- vote: voting web UI
- redis: message queue
- worker: background processor
- db: PostgreSQL database
- result: results web UI

Runtime flow:

```text
Browser -> vote -> Redis -> worker -> PostgreSQL -> result -> Browser
