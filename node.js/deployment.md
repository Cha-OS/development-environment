# Open Stack

## Deployment

+ kubernetes openstack
+ grpc openstack

### npm packages

+ [npm install private github repositories by dependency in package.json](https://stackoverflow.com/questions/23210437/npm-install-private-github-repositories-by-dependency-in-package-json)


+ Cloud Native
  + Computing Foundation
+ Docker
  + Container
+ Kubernetes
  + Orchestration
+ HELM
  + Package and deply
+ Prometheus
  + Monitoring
  + data store
  + visualization
    + graphit
    + graphona
      + dashboard build support
      + alerts 
+ Opentracing
  + distributed tracing



Goo

+ Borg
  + containers
+ **Kubernetes**
  + rewritten OS friendly Borg
  + written in Go
  + moves you from dealing with machines into dealing with cluster
+ Stubby
  + RPC between containers
+ **gRPC**
  + rewritten Stubby but using HTTP2 and protocol buffer 3
+ Johny5
  + node for IoT

[Building high performance microservices with Kubernetes, Go, and gRPC (Google Cloud Next '17)](https://www.youtube.com/watch?v=YiNt4kUnnIM)

+ ​

[Docker Swarm or Kubernetes or Mesos - pick your framework! by Arun Gupta](https://www.youtube.com/watch?v=1dgUXNVQS5o)

[Four Distributed Systems Architectural Patterns by Tim Berglund](https://www.youtube.com/watch?v=tpspO9K28PM)

[The hardest part of microservices is your data](https://www.youtube.com/watch?v=MrV0DqTqpFU)

[Managing Data in Microservices](https://www.youtube.com/watch?v=E8-e-3fRHBw)

[What Comes after Microservices?](https://www.youtube.com/watch?v=UDC3kwkBvkA)

[Mastering Chaos - A Netflix Guide to Microservices](Mastering Chaos - A Netflix Guide to MicroservicesInfoQ189K views)

[10 Tips for failing badly at Microservices by David Schmitz](https://www.youtube.com/watch?v=X0tjziAQfNQ)

[Neal Ford - Building Microservice Architectures](https://www.youtube.com/watch?v=pjN7CaGPFB4)

[Developing microservices with aggregates - Chris Richardson](https://www.youtube.com/watch?v=7kX3fs0pWwc)

[Martin Fowler – Microservices](https://www.youtube.com/watch?v=2yko4TbC8cI)

+ … law
  + design of organization will follow design of technology
  + MS therefore promotes few people directly responsible for their service and talking with customer
    + i.e. reputation service in Amazon
+ ESB - Enterprise Service Bus, SOA
  + have business logic in network orchestrating
  + services have very dump message-pipe only possible to deliver message to the provided address
+ conitnuous delivery
  + blue-green deployment
  + phoenix services
+ distributed objects
  + idea to treat RPC as local calls
  + wrong, local calls do not break
+ chaos-monkey
  + at netflix
  + a tool that randomly stop services
+ monoliths vs. micro-services
  + MS promotes using different storage, and data are always exchanded through service, never through database
  + RPC are additional complexity
  + micro-services are puting borders for refactoring
    + with monolitic code you can easier refactor
    + currently, successfull micro-services started as monolithic and then migrated to micro-services inccrementally
    + MS are supportinh modules easily
    + MS support different platforms and languages
+ necessary for successful MS
  + have servers provisioning fast (authomatic)
  + make support for monitoring
  + rapidly deployment of services in the provisioned servers
    + roll back quickly
      + old version of the service, if something is wrong
  + devops culture
    + this rises bar on operation-peple signifitcally

[Using sagas to maintain data consistency in a microservice architecture by Chris Richardson](https://www.youtube.com/watch?v=YPbGW3Fnmbc)

[An Overview of Designing Microservices - March 2017 AWS Online Tech Talks](https://www.youtube.com/watch?v=Ijs55IA8DIk)

[Principles Of Microservices by Sam Newman](https://www.youtube.com/watch?v=PFQnNFe27kU)

[What is Docker | Docker Tutorial for Beginners | Docker Container | DevOps Tools | Edureka](https://www.youtube.com/watch?v=lcQfQRDAMpQ)

+ ​

[Mesos vs Kubernetes vs Swarm: Fight! by Christophe Furmaniak](https://www.youtube.com/watch?v=DuGZ5UYHxI8)

+ ​

[GOTO 2016 • What I Wish I Had Known Before Scaling Uber to 1000 Services • Matt Ranney](https://www.youtube.com/watch?v=kb-m2fasdDY)

+ Heatmaps
+ any kind of representation on speed
+ a way to understand high-level picture
+ auto-generated and non-service specific dashboard
+ Tracing
  + Z… or OpenTracing

[Kubernetes in production - blue-green deployment, auto scaling and deployment automation](https://www.youtube.com/watch?v=-Ci4vd4rh4M)



# Clouds

## Nextcloud vs ownCloud

+ https://project-management.zone/system/nextcloud,owncloud
+ https://nextcloud.com/blog/3-reasons-to-upgrade-your-owncloud-instance-to-nextcloud-and-how-easy-it-is/
+ https://nextcloud.com/compare/
+ ​