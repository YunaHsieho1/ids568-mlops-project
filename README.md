# IDS 568 – Milestone 0

![CI](https://github.com/YunaHsieho1/ids568-mlops-project/actions/workflows/ci.yml/badge.svg)

## Overview
This repository is for Milestone 0 of the IDS 568 MLOps course. The purpose of this milestone 
is to set up a reproducible Python environment and a basic continuous integration (CI) workflow. 
This setup will be used as the foundation for future milestones in the course.

## Setup Instructions

### Requirements
- Python 3.11
- Git

### How to Set Up the Environment
```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Continuous Integration
GitHub Actions is used to automatically test the environment in a clean setup.
The CI workflow installs all dependencies and runs a simple smoke test to check
that required libraries can be imported correctly.

## Reproducibility and the ML Lifecycle

Reproducible environments are important for machine learning projects because models are often
developed on a local machine and later run in different environments such as server or cloud
platforms. During the ML lifecycle, code and models move across multiple stages, and
inconsistencies in dependencies can cause unexpected failures. If dependencies are not properly
controlled, code that works on one machine may fail on another, making debugging and deployment
more difficult.

In this project, reproducibility is achieved by pinning all Python dependencies to exact versions
in the requirements.txt file. This ensures that the same environment can be recreated consistently
by different users or automated systems. In addition, GitHub Actions is used to automatically install
the dependencies and run a simple smoke test in a clean environment. This helps verify that the setup
works independently of any local machine configuration.

These practices help reduce errors during deployment and provide a reliable starting point for later
stages of the ML lifecycle.
