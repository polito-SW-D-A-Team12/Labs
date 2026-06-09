# SDA Labs — MZinga Workers and Deployment Practices

## Overview

This repository contains the lab work developed for the Software Design and Architecture course.

The repository is organised using Git branches. Each lab has its own branch, while Lab 1 is located in the main branch.

## Branch Organisation

```text
Labs repository
├── main
│   └── Lab 1 — Initial worker implementation
│
├── lab2-partA
│   └── Lab 2 Part A — REST API email worker
│
├── lab2-partB
│   └── Lab 2 Part B — Event-driven email worker using RabbitMQ
│
├── lab3
│   └── Lab 3 — Observable worker with structured logs, metrics and traces
│
└── lab4
    └── Lab 4 — Kubernetes deployment strategies
```
## Lab Summary

### Lab 1 — Initial Worker

Branch: main

Lab 1 contains the first worker implementation and the initial project setup. It establishes the basic structure used later by the following labs.

### Lab 2 Part A — REST API Worker

Branch: lab2-partA

This lab implements a Python worker that polls the MZinga REST API for pending communications, sends emails through MailHog, and updates the communication status through the API.

### Lab 2 Part B — Event-Driven Worker

Branch: lab2-partB

This lab replaces polling with an event-driven architecture. The worker subscribes to RabbitMQ events emitted by MZinga and processes new communications when they are created.

### Lab 3 — Observability

Branch: lab3

This lab instruments the REST worker with observability features:

- Structured JSON logging
- OpenTelemetry traces exported to Jaeger
- Prometheus-compatible metrics
- HTTP request instrumentation
- Custom worker metrics for processed emails, polling and SMTP latency

### Lab 4 — Kubernetes Deployment Strategies

Branch: lab4

This lab deploys a simple containerised web application to Minikube and demonstrates four Kubernetes deployment strategies:

- Rolling Update
- Recreate
- Blue-Green Deployment
- Canary Release

The lab includes Kubernetes manifests for each strategy and shows how traffic changes during each deployment model.

## Environment Files

Some worker .env files are included in the repository.

Included:

text Lab worker .env files 

Not included:

text MZinga .env file 

## Testing Status

All labs have been implemented, tested locally and verified to work correctly.

Verified behaviours include:

- Lab 1 worker execution
- Lab 2 REST worker processing pending communications
- Lab 2 event-driven worker processing RabbitMQ communication events
- Lab 3 logs, metrics and traces
- Lab 4 rolling update, recreate, blue-green and canary strategies on Minikube

## Notes

Some files may differ between branches because each lab represents a different stage of the architecture.
