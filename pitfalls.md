# Pitfalls

Here’s a list of some of the pitfalls we’ve experienced when building Digital Platforms in partnership with various clients. We’d encourage you to avoid the scenarios listed below.

## On-premise Digital Platform

We’ve worked with several clients who tried to build a bespoke Platform as a Service on premises, as a means to leverage an investment in existing on-premises data centres. It’s proven to be a false economy every time.

Compared to a cloud provider, an on-premise data centre will suffer from:

* Slower capability delivery. Creating bespoke capabilities on top of low-level data centre abstractions will take weeks or months longer than in a public cloud.
* Less scalability. One-off, inelastic provisioning that is scaled for irregular peak traffic flows is cumbersome, and expensive.
* Higher maintenance costs. Maintaining and upgrading servers on a regular basis takes time away from platform feature development. 
* Higher operational costs. Covering data centre costs such as compute, energy bills, and staffing is expensive.

The costs associated with managing an on-premise Digital Platform can be exponentially higher than a Cloud Digital Platform. We strongly recommend the use of AWS, Azure, or GCP to underpin a Digital Platform.

## Premature Digital Platform team

We’ve seen well-intentioned organisations start a Digital Platform without a Digital Service team as a first user. A Digital Platform team working in a vacuum can spend weeks or months on platform capabilities with no stated needs from Digital Service teams. As a result, future Digital Service teams have to go their own way, without the economies of scale produced by a Digital Platform built in close consultation with Digital Service teams.

A Digital Platform team that lacks a Digital Service team can’t form any bi-directional feedback loops. It can’t understand the needs of its users, can’t set a direction for platform capabilities, and can’t validate the platform features that it builds. It’s just building automated infrastructure. This is why we believe [at least one Digital Service team at the outset](https://digital-platform.playbook.ee/introduction/when-to-start-a-digital-platform) as part of the startup criteria for a Digital Platform.

## Multi-instance Digital Platform

In some organisations, each Digital Service team runs their own instance of the Digital Platform, built by a central Digital Platform team. A Digital Platform team member may be embedded in each Digital Service team. Over time, this creates a Digital Platform ecosystem with significant operational costs and major challenges in culture, recruitment, and deploying updates to multiple instances of the Digital Platform.

Splitting Digital Platform team members between Digital Service teams will divide their focus, leading to large amounts of rework and duplication. As the number of Digital Service teams grows, it will prove difficult to recruit a Digital Platform engineer for each Digital Service team.

We prefer to have one instance of a Digital Platform run for all Digital Service teams by the Digital Platform teams. We believe this is the most effective way for Digital Platform and Digital Service delivery to happen in parallel. It makes it easier for Digital Platform team members to share knowledge and quickly respond to problems.

This does mean the Run A Service platform capability needs to ensure Digital Services are partitioned as much as possible to minimise failure blast radius. Partitioning might need some configuration \(e.g. [AWS EKS namespacing\)](https://aws.amazon.com/eks/), or it might come by default \(e.g. [GCP Cloud Run\)](https://cloud.google.com/run/).

## Proprietary library hell

A deployment pipeline will often include an artifact repository to host proprietary libraries, and a container image repository to host release candidates. A container image repository is essential for a container-based Run A Service capability. An artifact repository is not essential.

An artifact repository can encourage Digital Service teams to extract business logic and/or infrastructure logic into proprietary libraries. Over time, it gradually leads to [dependency hell](https://en.wikipedia.org/wiki/Dependency_hell) at scale, in which deployments are delayed by days or weeks due to painful library dependency changes.

As an alternative, we’d suggest Digital Platform teams produce a zero-friction Create a Service capability instead of an artifact repository. This will encourage Digital Service teams to produce more runnable monoliths or microservices, instead of proprietary libraries. They can still publish multi-consumer infrastructure logic as open-source libraries, albeit with a separate and entirely independent toolchain.

## Industrialised End-To-End Testing

We’ve worked with many clients to decrease their reliance on automated [End-To-End Testing](https://www.stevesmith.tech/blog/end-to-end-testing-considered-harmful/) in test environments. Continuous Delivery can’t be achieved when a production deployment requires days or weeks of functional testing with third-party systems.

If a Digital Platform allows Digital Service teams to self-provision unconstrained test environments, it’s easy for Digital Service teams to lapse into functional testing with third parties. As test execution times and determinism are inversely proportional to test scope, such an industralisation of End-To-End Testing makes Continuous Delivery very unlikely.

We recommend the following instead:

* Digital Platform teams produce high quality monitoring and alerting in production, and circuit breakers on the wire.
* Digital Service teams are incentivised to monitor live interactions with third parties, and gracefully degrade their services when necessary.
* Digital Platform teams create a curated pipeline with minimal test environments, such as a stubs environment with no end points for automated tests and an integration environment with third-party end points for exploratory testing only.
* Digital Service teams are encouraged to think of live monitoring of third parties as a superior alternative to End-To-End Testing.

