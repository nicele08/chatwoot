# Chatwoot Development Setup Guide

Welcome to the Chatwoot development setup guide! This document will walk you through the process of setting up and running Chatwoot in your local environment for development purposes.

## Prerequisites

Before you begin, please ensure that you have completed the environment setup as per the project requirements.

## Clone the Repository

First, clone the Chatwoot repository to your local machine:

```bash
# Change location to the path where you want Chatwoot to be installed
cd ~

# Clone the repository and navigate to the Chatwoot directory
git clone https://github.com/nicele08/chatwoot
cd chatwoot
```

## Install Ruby & Javascript dependencies

Use the following command to run `bundle && yarn` to install ruby and Javascript dependencies.

```bash
make burn
```

This would install all required dependencies for Chatwoot application.

## Setup environment variables.

```bash
cp .env.example .env
```

## Setup rails server

```bash
# run db migrations
make db
# fireup the server
foreman start -f Procfile.dev
```

Note: If you have overmind installed, use `make run` to run the server.

## Login with credentials

```bash
http://localhost:3000
user name: john@acme.inc
password: Password1!
```

## Testing chat widget in your local environment

When running Chatwoot in development environment, the chat widget can be accessed under the following URL.

```bash
http://localhost:3000/widget_tests
```

You can also test the setUser method by using

```bash
http://localhost:3000/widget_tests?setUser=true
```
