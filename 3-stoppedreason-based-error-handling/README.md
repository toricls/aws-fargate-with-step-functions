# Parallelized Fargate tasks with Step Functions "Map"

## Overview by Step Functions Workflow Studio

![overview](./overview.png)

## What you can do with this example

You can decide to or not to retry based on the specific error codes recorded in the "[stoppedReason](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/stopped-task-errors.html)" field which is produced from Fargate tasks.

For example, you can do "Retry when the error is `ResourceInitializationError`, but do not retry and just fail when the error is `CannotPullContainerError`". See the full list of the error codes in the [Amazon ECS documentation](https://docs.aws.amazon.com/AmazonECS/latest/userguide/stopped-task-error-codes.html).

## Set up

Use the [CloudFormation template](./template.yml) to provision resources.

## Run State Machine

Just run the state machine, then it always fails. Because the ECS task definition uses a non-existing container image name intentionally.

## Execution Result

![result](./result.png)
