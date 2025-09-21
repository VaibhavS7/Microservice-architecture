### Where Did Microservices Come From?

Well, the problems with monolithic architecture and the SOA (Service-Oriented Architecture) paradigm made it clear: we needed something new---something that could finally address these long-standing issues.

It became evident that this "something" had to be **modular**, because the monolithic model showed us exactly what happens when software lacks modularity.

It also had to offer a **simple API**, because SOA taught us the consequences of overcomplicated interfaces.

New ideas began to emerge, aiming to define a new kind of architecture---one that would meet these requirements and also address the other challenges we've discussed.

Then, in **2011**, the term **"microservices"** made its first appearance. It surfaced during a software architecture workshop and marked one of the earliest efforts to define what this new paradigm could and should look like.

But the real breakthrough came three years later, in **2014**.

That year, **Martin Fowler**, one of the most influential software architects, and his colleague **James Lewis**, published their now-famous **microservices article**.

In this article, they not only described the philosophy behind the microservices architecture, but---more importantly---they outlined the **key attributes** of such a system.

In essence, they said to the world:

> *"If you want to design a microservices architecture, here's how you do it."*

This article quickly became the **de facto standard** for defining microservices. Even though it was published years ago, it's still considered one of the most accurate and practical guides to understanding and implementing microservices today.

You can read the article here [(link)](https://martinfowler.com/articles/microservices.html), but you don't have to.

### What's Coming Next?

In the next section, we'll walk through the **nine core attributes** outlined in the article. We'll explain each one in detail, with real-world examples.

We'll also explore where these attributes may not be as straightforward as they seem---and what you *really* need to pay attention to when designing a microservices architecture.

Finally, we'll **rank these characteristics**, discussing which ones are truly essential and which might be less critical, depending on your context.

### The Nine Characteristics of a Good Microservices Architecture (According to Martin Fowler & James Lewis)

Here they are:

1.  **Componentization via Services**
2.  **Organized Around Business Capabilities**
3.  **Products, Not Projects**
4.  **Smart Endpoints and Dumb Pipes**
5.  **Decentralized Governance**
6.  **Decentralized Data Management**
7.  **Infrastructure Automation**
8.  **Design for Failure**
9.  **Evolutionary Design**