Kubernetes Documentation / Concepts / [Overview](https://kubernetes.io/docs/concepts/overview/)

## Kubernetes provides you with:

- Service discovery and load balancing: Kubernetes can expose a container using the DNS name or using their own IP address. If traffic to a container is high, Kubernetes is able to load balance and distribute the network traffic so that the deployment is stable.
- Storage orchestration: Kubernetes allows you to automatically mount a storage system of your choice, such as local storages, public cloud providers, and more.
- Automated rollouts and rollbacks: Declaratively describe what you want, and Kubernetes can change the actual state to the desired state at a specified rate. Example: Create new containers, remove existing containers, and link all their resources to the new container
- Automatic bin packing: Provide Kubernetes with a cluster of nodes to run containerized tasks, and declaratively tell Kubernetes how much CPU and RAM each container needs. Kubernetes can fit containers onto your nodes to optimize resource usage.
- Self-healing: Kubernetes restarts containers that fail, replaces containers, kills containers that don't respond to your health check, and doesn't expose them to clients until they're ready to serve
- Secret and configuration management: Store and manage passwords, tokens, and keys. Deploy and update secrets and app configuration without rebuilding container images or exposing secrets.
- Batch execution: Can manage batch and CI workloads, replacing containers that fail
- Horizontal scaling: Scale app up and down with a command, a UI, or automatically based on CPU usage
- IPv4 and IPv6 support

## What Kubernetes is not 

Kubernetes is not a traditional, all-inclusive PaaS (Platform as a Service) system. Since Kubernetes operates at the container level rather than at the hardware level, it provides some generally applicable features common to PaaS offerings, such as deployment, scaling, load balancing, and lets users integrate their logging, monitoring, and alerting solutions. However, Kubernetes is not monolithic, and these default solutions are optional and pluggable. Kubernetes provides the building blocks for building developer platforms, but preserves user choice and flexibility where it is important.

Kubernetes:

- Doesn't limit the types of application supported--stateless, stateful, and data-processing workloads are all supported--anything that can run in a container
- Doesn't deploy source code or build you app. That's left to CI/CD.
- Doesn't provide application-level services such as middleware (e.g., message buses), databases, caches, or cluster storage. Those components can run on Kubernetes or e.g. [Open Service Broker](https://openservicebrokerapi.org/).
- Doesn't dictate logging, monitoring, or alerting (observability).
- Doesn't provide a configuration language or system. Instead, provides a declarative API.
- Doesn't provide any comprehensive machine configuration, maintenance, management, or self-healing systems.
- Replaces orchestration (execution of a defined workflow) with declarative desired state specification, which Kubernetes then drives towards.

Containers:

- Are lightweight because they can share the operating system (OS) among the applications.
- Allow agile application creation and deployment: Easier and more efficient than VM images
- Continuous development, integration, and deployment: Reliable, frequent container image build and deployment with quick and efficient rollbacks because images are immutable
- Separation of concerns between Dev and Ops: Create images at build time instead of deployment time; decouples apps from infrastructure.
- Observability: Surfaces OS- and app-level information, metrics, and health
- Consistent environment across dev, test, and prod: Runs the same on a laptop as in the cloud
- Runs the same regardless of cloud and OS
- App-centric management: Level of abstraction is app on OS using logical resources, not OS on virtual hardware
- Loosely coupled, distribute, elastic, liberated micro-services: Apps are broken into smaller, independent peices that can be delplyed and managed dynamically--not a monolithic stack running on one big single-purpose machine
- Resource isolation: Predictable app performance
- Resource utilization: High efficiency and density
