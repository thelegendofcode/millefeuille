# Budgeteer

The final goal is an app for planning budgets. For the immediate future, the plan is to have a portfolio visualiser.

## How to install

1. git clone the repo
1. set up a GCP/Firebase account
1. deploy to Google Cloud Hosting

## How to run

Data is stored in Firebase while the client is hosted in GCP, so just access the address on the GCP dashboard.

Locally, run `yarn start` from the command line. This will build and run the client locally on your machine. Internet connection is still required because of Firebase usage.

## Features
### Is it multi-user?

A single instance can serve multiple users.

Each user may also create an instance for their own use.
