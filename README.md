# Lab 2 Part B — Event-Driven Email Worker

## Overview

This lab implements an event-driven Python email worker.

Instead of polling the MZinga REST API periodically, the worker listens to RabbitMQ events. When a new Communication is created, MZinga publishes an event and the worker processes it.

## Branch

```text
lab2-partB
