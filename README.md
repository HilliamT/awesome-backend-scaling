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
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Native Integration with AWS Cloudwatch</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Native Cloud Monitoring with Google Cloud Platform</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>API Monitoring with Postman</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Website Monitoring with Better Uptime</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Kubernetes Cluster Monitoring</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
    </tbody>
</table>

#### Resources Monitoring
A service may also not be down, but it may be experiencing a degradation in performance as it does not have enough resources to handle a certain intended workload. Monitoring resource usage can help you identify when this happens.
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
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Flame Graphs</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Infrastructure Monitoring with Datadog</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Native Integration with AWS Cloudwatch</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Native Cloud Monitoring with Google Cloud Platform</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Kubernetes Metrics Server</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
    </tbody>
</table>

#### Observability
Whilst monitoring tells you if a service is suffering an issue, observability aims to provide you with details on why the issue is occurring.
<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Logging to Console</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Logging to an API endpoint</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Logtail</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Splunk</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Datadog</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>New Relic</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>AppDynamics</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
    </tbody>
</table>

## Execution
Increasing the capacity of your application can be a key step to solving bottlenecks. This will generally optimise the performance of your application, but you should compare this to other more-dedicated solutions that may be more cost-effective.

#### Vertical Scaling
Vertical scaling focuses on allocating more resources to a single instance. Included also are considerations to optimise resource usage on an instance-granular level.
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
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Changing Programming Language</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Code Optimisation</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Increase Server RAM</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Change Server Processor Type</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Increase Number of Cores</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
    </tbody>
</table>

#### Horizontal Scaling
Horizontal scaling notices that there is a limit to how many resources you can dedicate to a single instance and therefore utilises the resources of other instances to meet the demand.
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
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Kubernetes Pod Scaling</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Cloud Functions</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
    </tbody>
</table>

## Internal Messaging
When a system contains different services that are ran as separate processes, they may need to communicate with each other. This can be achieved by using a messaging system. Even if storage on individual services may be large, a system is bottlenecked by the bandwidth of data transfer.

#### Communication Protocol
The format of a message can be important in efficiency based on the use case.
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
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Websockets</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Data Streaming</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>gRPC</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>On-Trigger Cloud Functions</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
    </tbody>
</table>

#### Message Delivery
There are more specialised messaging systems that can be used to deliver messages based on need. These generally tend to be towards several services that may be dynamically scaled. Maintenance of updating the endpoint to call can be a bottleneck in developer resources too.
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
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>API Gateways</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Bi-directional APIs with Pusher</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>RabbitMQ Messaging Queues</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Message Brokers on Apache Kafka</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Google Pub/Sub</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
        <tr>
            <td><strong>Istio and Service Meshes</strong></td>
            <td><code>🚧 TODO 🚧</code></td>
        </tr>
    </tbody>
</table>

## Storage
`🚧 TODO 🚧`

#### Online Transaction Processing (OLTP)
<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>In-Memory</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Redis Caching</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>PostgresDB</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>MongoDB</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Cassandra</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Search Engine Elasticsearch</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>PgBouncer for PostgresDB</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>PgPool</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Database Sharding</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Cloud Databases</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Google Cloud SQL</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Amazon DynamoDB</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Mission-critical Transactional Consistency with Google Spanner</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Large-Scale Low-Latency with Google Cloud Bigtable</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

#### Online Analytics Processing (OLAP)

<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>General Databases</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Elasticsearch</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Data Warehouses</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Data Lakes</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

#### Archival
<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>General Databases</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Cold Storage</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Arweave: Archiving on the Blockchain</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>


## External Endpoints
`🚧 TODO 🚧`
#### Rate Limiting
`🚧 TODO 🚧`

#### Endpoint Handler
`🚧 TODO 🚧`

## Scheduling
`🚧 TODO 🚧`

## Authentication and Authorisation
`🚧 TODO 🚧`

## Robustness
`🚧 TODO 🚧`

#### Testing

<table>
    <thead>
    <tr>
        <th>Approaches</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Unit Testing</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Component Testing</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Integration Testing</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>End-to-End Load Testing</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Web Performance Testing</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Stress Testing</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Fuzzing</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Symbolic Execution</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Static Analysis</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Formal Verification</strong></td>
            <td></td>
        </tr>
        <tr>
            <td><strong>Chaos Engineering for Microservices</strong></td>
            <td></td>
        </tr>
    </tbody>
</table>

## Resources
These books and articles have been helpful in my development of this guide:

- [API Security in Action](https://www.manning.com/books/api-security-in-action)