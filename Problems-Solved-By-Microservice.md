## Single Technology Platform

### Overcoming the Single Technology Platform Limitation with Microservices

One of the significant challenges with monolithic architectures is the **Single Technology Platform** constraint.

In a monolith, all components must be developed using the same technology stack. Because a monolith operates as a single process, you cannot build different parts of the application using different platforms. This restriction can limit flexibility and innovation.

Often, we want to leverage multiple platforms within a single application to take advantage of each platform's unique strengths. However, with a monolith, this is simply not possible - you are locked into your initial technology choice for the entire application.

For instance, if your monolith was developed using Java 8 and you want to upgrade to Java 9, you must upgrade the entire application simultaneously. This makes future upgrades complex and costly.

Similarly, if your monolithic app is built on .NET Core, you cannot incorporate components developed in Node.js or any other platform.

### How Microservices Solve This Problem

The Microservices architecture addresses this issue through the attribute of **Decentralized Governance**.

Decentralized Governance empowers each team to choose the most appropriate development platform for their specific microservice. Teams are not restricted by a central mandate dictating which language, database, or messaging system to use. Instead, they have the freedom to select technologies based on the service's requirements, provided there is a valid reason for the choice (note: using a technology simply because it's "new and shiny" is not a good reason).

For example, in a microservices-based system:

-   Some services might be developed using .NET Core.
-   Others might be built with Node.js, Python, Java, Rust, or any other suitable platform.
-   This flexibility enables teams to innovate faster and leverage the best tools for their service's needs.

### The Result: Technology Diversity Without Compromise

Thanks to Decentralized Governance:

-   Each microservice can be developed and maintained independently.
-   Different platforms coexist harmoniously within the same application ecosystem.
-   Teams can upgrade or switch platforms for individual services without impacting the entire system.

In summary, **Decentralized Governance** in microservices architecture effectively overcomes the Single Technology Platform limitation inherent in monolithic systems, enabling a more flexible, scalable, and future-proof approach to application development.


## The Next Challenge: Inflexible Deployment

One of the common problems with monolithic applications is **inflexible deployment**.

-   With a monolith, whenever you deploy the application, you have to deploy the entire app.
-   There is no option to deploy only a part of the application.
-   This means that even if you update just one component, you must redeploy the whole codebase.
-   As a result, every deployment requires rigorous testing of the entire application.
-   This often leads to longer development cycles and slower release times.

### How Do Microservices Handle Deployment Differently?

The key attribute that addresses this issue is **Componentization via Services**.

-   By modeling your system as a collection of independent services (rather than libraries), it becomes much easier to deploy just one part of the system.
-   Each microservice runs as a separate process, reducing coupling between components.
-   This separation allows each microservice to be deployed independently without impacting others - unless there is a major breaking API change.

For example, in a Microservices architecture:

-   Each service runs in its own process.
-   Each can be updated and deployed separately.
-   This leads to **flexible and faster deployments**.

### The Role of Decentralized Data Management

Another important factor contributing to flexible deployment is the **Decentralized Data Management** attribute:

-   Each microservice manages its own database.
-   This means deploying an updated service along with its own updated database is easier and isolated.
-   If the system had a single unified database, any change would potentially affect other services, causing tight coupling.
-   Separate databases ensure each service remains an independent deployment unit.

### Summary: How Microservices Solve Inflexible Deployment

-   Microservices allow **independent deployment** of components thanks to their process isolation.
-   Decentralized data management ensures **database changes do not cascade** across services.
-   Together, these attributes enable faster, safer, and more flexible deployments compared to monolithic applications.

## Inefficient Compute Resource

### Tackling Inefficient Compute Resource Usage with Microservices

Our next challenge is **inefficient use of compute resources** - specifically CPU and RAM.

In a monolithic application, all components run within a single process, sharing the same pool of compute resources.

-   The monolith consumes CPU and memory collectively for all its internal components.
-   This setup isn't always ideal.
-   For example, if one component requires more CPU or memory, there's no way to allocate extra resources specifically to that component.
-   Instead, you must allocate more resources to the entire monolith, which means all components get the extra resources, whether they need them or not.
-   This approach leads to inefficient resource utilization and potential waste.

### How Microservices Provide a Better Solution

With microservices, the **Componentization via Services** attribute helps us solve this problem.

-   Each component runs as an independent service in its own process, rather than as part of a single monolithic process.
-   While it's not possible to allocate resources to individual code segments inside a process, you can allocate resources to entire processes.
-   Since each microservice runs in its own process, you can assign compute resources - CPU, memory, and so on - tailored to the needs of each service.

### Example of Resource Allocation in Microservices

Imagine a microservices system with five services, each running in its own process.

-   Some services with low resource demands might be allocated **2 vCPUs and 4 GB of RAM**.
-   Others, which perform heavy computations, might be assigned **8 vCPUs and 16 GB of RAM**.
-   This allocation flexibility enables better resource efficiency and cost-effectiveness.

### Conclusion

By running services independently, microservices architectures allow you to allocate compute resources precisely where they are needed, avoiding the inefficiencies common in monolithic systems.

This is how microservices effectively solve the problem of inefficient compute resource usage.

## Large and Complex Problem

### Tackling the Large and Complex Problem with Microservices

One of the major challenges with monolithic applications is their **large and complex codebase**.

Since all software components are part of a single process:

-   The codebase naturally becomes very large.
-   It contains many dependencies and tight coupling between components.
-   Even small changes can inadvertently affect other parts of the system.
-   This leads to extensive testing requirements to ensure nothing breaks.
-   Despite thorough testing, bugs can still slip through, making maintenance difficult.
-   The lengthy verification process turns every small change into a daunting task.
-   Consequently, developers may avoid making changes, causing the system to become obsolete quickly.

### How Microservices Help Simplify Complexity

The key attribute here is **Componentization via Services**.

-   By modeling your system as a collection of services running out-of-process, each service becomes a well-defined, bounded piece of code.
-   These boundaries are strict because each service runs in its own process and cannot directly access code from other services.
-   This isolation naturally reduces coupling and complexity within the codebase.
-   Each service can be maintained independently, making changes safer and easier.

### Additional Isolation through Decentralized Data Management

Another important attribute is **Decentralized Data Management**:

-   Each microservice manages its own database.
-   This prevents the mixing of data and functionality that often occurs in a shared, monolithic database.
-   Without this separation, complexity and coupling simply shift from the codebase to the database.
-   Separate databases keep both code and data small, simple, and easier to maintain.

### Organized Around Business Capabilities

The **Organized Around Business Capabilities** attribute also plays a crucial role:

-   Each service is owned by a dedicated team responsible for all aspects: UI, API, business logic, data access, database, and testing.
-   This eliminates slow, cumbersome communication between different groups.
-   Teams can work autonomously and efficiently, increasing the chance that the service remains simple and maintainable.

### Summary: How Microservices Solve the Large and Complex Problem

-   Services are **well-bounded**, isolated units of code.
-   Data is **decentralized**, preventing cross-service data entanglement.
-   Teams are **organized around business capabilities**, fostering ownership and streamlined development.

Together, these attributes reduce complexity, improve maintainability, and make the system easier to evolve.

This is how microservices effectively solve the large and complex problem inherent in monolithic architectures.

## Complicated and Expensive ESBs

### The Problem with Complicated and Expensive ESBs

In Service-Oriented Architecture (SOA), the **Enterprise Service Bus (ESB)** plays a central role in managing communication between various applications or services.

However, ESBs often become:

-   Bloated and overly complex,
-   Expensive to maintain,
-   Overloaded by handling too many responsibilities such as routing, validation, authentication, and more.

When a single component tries to handle everything, it often leads to a fragile and difficult-to-manage system.

Many organizations end up investing significant time and money just to keep the ESB running smoothly, which becomes a major bottleneck.

### How Microservices Solve the ESB Problem

The attribute that addresses this issue is the **Smart Endpoints and Dumb Pipes** principle.

-   In microservices, communication responsibilities are pushed to the services themselves.
-   The communication mechanism is kept simple and straightforward.
-   Typically, this is achieved using **REST**, which is based on the widely adopted HTTP protocol---leveraging existing, proven communication standards rather than reinventing the wheel.

### What Does This Look Like?

In a microservices system following this principle:

-   Multiple services communicate directly with one another using simple RESTful APIs.
-   There is no need for a complex, centralized ESB to mediate interactions.
-   Services handle their own communication logic without relying on an expensive intermediary.

### Modern Communication Patterns in Microservices

While the **Smart Endpoints and Dumb Pipes** attribute encourages simple communication, the microservices ecosystem has evolved:

-   Direct service-to-service communication is now often discouraged.
-   Instead, patterns like **API Gateway** and **Service Discovery** are used to manage service interactions more efficiently (these will be covered later in this course).

Additionally, although REST is popular, new API protocols have emerged that offer capabilities beyond REST, such as:

-   **GraphQL** (developed by Facebook): Supports dynamic querying and reduces over-fetching.
-   **gRPC** (developed by Google): Supports efficient communication with features like push notifications and streaming.

These newer APIs are rapidly gaining popularity and are worth exploring as alternatives or complements to REST.

### Summary

By adopting the **Smart Endpoints and Dumb Pipes** principle, microservices eliminate the need for complicated and expensive ESBs, leading to simpler, more maintainable, and cost-effective communication architectures.

## The Last Problem: Lack of Tooling

As we've discussed, **Service-Oriented Architecture (SOA)** needed to enable **short development cycles** to be truly effective.

-   One of the major issues with monolithic architectures was their long development and deployment cycles.
-   SOA promised improvement by allowing faster testing and deployment.
-   However, for SOA to deliver on this promise, it required **tooling to support automation** in testing and deployment.
-   Unfortunately, such tools were largely unavailable at the time.
-   As a result, SOA did **not achieve meaningful time savings**, which frustrated developers and contributed to its limited adoption and eventual decline.

### How Do Microservices Address This?

The Microservices movement directly tackles this challenge through the **Infrastructure Automation** attribute.

-   This attribute focuses on automating **testing** and **deployment**---the key components of the deployment cycle.
-   Automation tools enable **short, reliable deployment cycles**, one of the main advantages of Microservices.
-   By automating these processes, Microservices architectures become more efficient, agile, and responsive to change.

### Why Automation Matters

-   Automation is a **core capability** of any Microservices-based system.
-   As an architect or developer, it is critical to **never compromise** on infrastructure automation.
-   Embracing automation solves the tooling gap that hindered SOA and monolithic approaches.

### Summary

With automation at its heart, Microservices overcome the tooling challenges that plagued earlier architectures, enabling fast, reliable, and continuous delivery.

### Additional Problems Microservices Can Solve

1.  **Scalability Challenges**

    -   Monoliths often force scaling the entire application even if only certain components need more resources.
    -   Microservices allow **independent scaling** of each service based on its own demand, optimizing resource usage and cost.

2.  **Fault Isolation and Resilience**

    -   In monoliths, a failure in one component can bring down the entire system.
    -   Microservices isolate failures to individual services, improving overall system resilience and fault tolerance.

3.  **Technology Diversity and Experimentation**

    -   Beyond just the single technology platform problem, microservices enable teams to **experiment with new tools and frameworks** safely without impacting the entire system.
    -   This fosters innovation and faster adoption of emerging technologies.

4.  **Faster Time-to-Market for Features**

    -   Smaller, independently deployable services allow teams to **develop, test, and deploy features faster**.
    -   Reduces bottlenecks often seen with large teams working on one codebase.

5.  **Organizational Alignment and Autonomy**

    -   Microservices map well to **small, cross-functional teams** owning full lifecycle of their service (DevOps culture).
    -   This leads to better team ownership, faster decision making, and less coordination overhead.

6.  **Easier Maintenance and Upgrades**

    -   Small, focused codebases are easier to understand, maintain, and upgrade over time.
    -   Reduces technical debt compared to large monolithic codebases.

7.  **Improved Security Boundaries**

    -   Services can have tailored security policies and access controls.
    -   Limits blast radius if a security breach occurs in one service.

8.  **Better Alignment with Cloud-Native Practices**

    -   Microservices fit naturally with containerization, orchestration (e.g., Kubernetes), and cloud infrastructure.
    -   Enables advanced capabilities like rolling updates, canary deployments, and autoscaling.

This completes our overview of how Microservices solve key problems inherited from monolithic and service-oriented architectures.