# Zero downtime architecture

## Design
1. PostgreSQL cluster, 1 write node, 2 read nodes
2. Microservices/Highly decoupled services
3. Client app supports retry

## High availability
During a major deployment that includes database migration, the PostgreSQL master node is paused from writes, hence:
1. Only allows read operations
2. Write operations are queued
