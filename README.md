# MLOps Ansible Demo

This repository contains an Ansible playbook for setting up a MLOps environment on a Kubernetes cluster.
This also describes core concepts of Ansible for the MLOps project.

## Summary

We'll build a mini-project that:
- Defines an **inventory** of ML hosts
- Uses an **ansible.cfg** to configure **connection** and **callback plugins**.
- Containes a top-level **site.yml playbook** leveraging the **collections** keyword for `community.general` and `community.docker`.
- Declares three **Plays**, each calling a **Role**:
1. `ml_enviroment` (sets up a Python, virtualenv, ML libs)
2. `mlflow_server` (installs & configures MLFlow as a service)
3. `model_deploy` (packages and runs a Dockerized model API)
- Within each **Role**, organizes **Tasks** (actions via **Modules**), **Handlers** (triggered on change), plus a demonstration of a **lookup plugin** (env) and a **filter plugin** (flatten).
- Follows a **filetree** matching Ansible best practices.

## Prerequisites

- A Kubernetes cluster
- Ansible CLI
- Python 3.10+
- Docker CLI
- Git CLI

