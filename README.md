# Udagram on an AWS pipeline

Deployment project from the EGFWD fullstack track. The app itself, an Angular frontend with a Node/Express API, came from Udacity as a starter. My work was everything around it: the AWS infrastructure, the CircleCI pipeline, and making a push to main deploy both halves automatically.

[![CircleCI](https://circleci.com/gh/Ibrahim-Rezq/udagram-full-stack.svg?style=svg)](https://app.circleci.com/pipelines/github/Ibrahim-Rezq/egfwd-udagram-aws-pipeline?branch=main&filter=all)

![Website screenshot](https://github.com/Ibrahim-Rezq/egfwd-udagram-aws-pipeline/blob/main/Documentation/Screenshots/Website.png)

## The infrastructure

Three AWS pieces, each doing one job:

- The Angular build sits on S3 as a static site
- The Express API runs on Elastic Beanstalk
- PostgreSQL lives on RDS

![Infrastructure diagram](https://github.com/Ibrahim-Rezq/egfwd-udagram-aws-pipeline/blob/main/Documentation/Screenshots/Udagram_Diagram.png)

## The pipeline

Push to main and CircleCI takes it from there: build the Angular app, build the TypeScript backend, deploy the frontend to S3 and the backend to Elastic Beanstalk. No manual deploy steps.

![Pipeline diagram](https://github.com/Ibrahim-Rezq/egfwd-udagram-aws-pipeline/blob/main/Documentation/Screenshots/Pipeline_Diagram.png)

## Running it locally

You'll need Node 14+, the AWS CLI configured, and Angular CLI 12.

```bash
npm run front-end-install   # Angular dependencies
npm run back-end-install    # Node dependencies
```

Useful scripts:

```bash
npm run front-end-build     # build the Angular app
npm run front-end-deploy    # push it to S3
npm run back-end-build      # compile the backend
npm run back-end-deploy     # push it to Elastic Beanstalk
npm run setEnv              # set environment variables
```

## Stack

Angular, TypeScript, Node, Express, PostgreSQL. AWS S3, Elastic Beanstalk, and RDS for hosting. CircleCI for the pipeline.
