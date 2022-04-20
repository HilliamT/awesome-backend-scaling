# Awesome Backend Scaling

- [Motivation](#motivation)
- [Monitoring and Observability](#monitoring-and-observability)
- [Execution](#execution)
- [Internal Messaging](#internal-messaging)
- [Storage](#storage)
- [External APIs](#external-apis)
- [Scheduling](#scheduling)
- [Authentication and Authorisation](#authentication-and-authorisation)
- [Robustness](#robustness)
## Motivation

As an application grows in users, it can face problems that limit its capacity to grow with this demand. Bottlenecks in the system may start being observed that degrade the performance for users:

- Slow requests to load your social media timeline due to high load on the database
- Verification emails not being sent because the email-send worker is overloaded
- Timeouts being hit for API requests leading to failed checkouts

These and many more can deter users away and affect how well you meet your business KPIs.

This guide aims to collate various practices and approaches, some used, to solve different types of bottlenecks. Some may be applicable or not - take what you will.

## Monitoring and Observability
Knowing that there is a degradation in performance is the first key step to being able to identify solutions for it.

Systems often rely on different services to provide certain functionalities. You may have an authentication server to dedicated to managing authentication for users. You may have an API server for delivering data to your mobile app. Services like these are integral to making your application work.

If a service has crashed due to an uncaught software bug or a hardware failure, this can be detrimental.


## Execution
`🚧 TODO 🚧`

## Internal Messaging
`🚧 TODO 🚧`
## Storage
`🚧 TODO 🚧`

## External Endpoints
`🚧 TODO 🚧`

## Scheduling
`🚧 TODO 🚧`

## Authentication and Authorisation
`🚧 TODO 🚧`

## Robustness
`🚧 TODO 🚧`

## Resources
These books and articles have been helpful in my development of this guide:

- [API Security in Action](https://www.manning.com/books/api-security-in-action)