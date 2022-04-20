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

#### Health Monitoring

To check if a service has crashed, intermittent calls to the service can be made. If the service is not responding, it is likely to be down.

`🚧 TODO 🚧`

<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Manual Heartbeats</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Native Integration with AWS Cloudwatch</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Native Cloud Monitoring with Google Cloud Platform</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>API Monitoring with Postman</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Website Monitoring with Better Uptime</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Kubernetes Cluster Monitoring</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

#### Resources Monitoring
`🚧 TODO 🚧`
<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Cron Job</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Infrastructure Monitoring with Datadog</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Native Integration with AWS Cloudwatch</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Native Cloud Monitoring with Google Cloud Platform</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Kubernetes Metrics Server</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

#### Observability
`🚧 TODO 🚧`
<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>console.log</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Logging to an API endpoint</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Logtail</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Splunk</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Datadog</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>New Relic</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>AppDynamics</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

## Execution
`🚧 TODO 🚧`

#### Vertical Scaling
`🚧 TODO 🚧`
<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Caching</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Changing Programming Language</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Code Optimisation</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Increase Server RAM</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Change Server Processor Type</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Increase Number of Cores</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

#### Horizontal Scaling
`🚧 TODO 🚧`
<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Moving to a Microservice Architecture</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Kubernetes Pod Scaling</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Cloud Functions</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

## Internal Messaging
`🚧 TODO 🚧`

#### Communication Protocol
<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>HTTP REST</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Websockets</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Data Streaming</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>gRPC</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

#### Message Delivery
<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Inline API Calls</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>API Gateways</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Bi-directional APIs with Pusher</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>RabbitMQ Messaging Queues</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Message Brokers on Apache Kafka</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Google Pub/Sub</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Istio and Service Meshes</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>On-Trigger Cloud Functions</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

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