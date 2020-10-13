# Paved Road

### Pave the pain points

It’s difficult to know in which order to add platform capabilities to the Paved Road. An entire user journey such as Test A Service could be paved in one go, resulting in a long and narrow Paved Road that gradually widens. Alternatively, different parts of different user journeys could be paved, producing a short and wide Paved Road that gradually lengthens.

It’s also difficult to know how much of a platform capability needs to be paved – that is, how much the Digital Platform teams will manage centrally versus how much the Digital Service teams will manage for themselves. More central management means more paving and less boilerplate for Digital Service teams, which can produce tangible benefits:

* Digital Service teams are freed up to concentrate on Digital Service business logic
* Consistent patterns for builds, testing, monitoring, and alerting can all be rolled out
* The cognitive load for new joiners and movers between Digital Service teams is much lower
* Digital Platform teams are able to silently and rapidly roll out updates 

On the other hand, more central management also means:

* The technical quality of the Digital Platform has to be of a very high standard, otherwise Digital Service teams are likely to perceive it as a constraint 
* Digital Service teams can be unhappy if they have little say in the processes and tooling that comprise their user journeys

This is why user feedback and experimentation is so important, as with any product development. Digital Platform teams that run small, frequent experiments on platform capabilities, powered by their own hypotheses and user feedback from Digital Service teams will quickly learn which capabilities will be most beneficial. Prioritising the paving of the biggest pain point for a majority of Digital Service teams at that point in time will help all of those teams. 

For example, the Run A Service capability might begin with an opinion that all code must be Kotlin. This would result in a centrally automated Docker image containing a Java Virtual Machine \(JVM\) instance, configured for Kotlin. Over time, the opinions behind Run A Service might include a particular database, a web framework, a metrics pipeline, and more. 

A Paved Road needs to be adaptable. It depends on a malleable platform architecture, with well-defined and testable boundaries for Digital Service teams. Raw cloud services from the cloud provider need to be leaked out in a controlled way, based on where Digital Platform abstractions cannot create additional value and where lock-in switching costs are low.

### Intentional friction as guard rails

Building a Digital Platform is about removing friction from paved user journeys, on behalf of Digital Service teams. At times, that also means adding intentional friction away from the Paved Road, to discourage Digital Service teams from adopting suboptimal practices.

It’s likely a majority of Digital Service team members won’t have worked on a Digital Platform before, won’t be familiar with Continuous Delivery practices, and won’t have operated a live customer-facing service before. It’s important that guardrails be established to reinforce the opinionated nature of the Digital Platform, and point Digital Service teams towards success.

Recommendations we’ve incorporated into Digital Platforms include the following:

* Don’t install a repository for proprietary libraries. This discourages the sharing of internal libraries between teams, and avoids the [proprietary library hell pitfall](https://digital-platform.playbook.ee/pitfalls#proprietary-library-hell)
* Don’t permit automated end-to-end tests in a test environment. This discourages reams of functional end-to-end tests, and avoids the [Industrialised End-To-End Testing pitfall](https://digital-platform.playbook.ee/pitfalls#industralised-end-to-end-testing)

It may take time for Digital Service teams to understand the purpose of intentional friction. It’s important for Digital Platform teams to engage with Digital Service teams, so they understand the purpose of intentional friction and can offer feedback.

### Design for optional Digital Service upgrades

Inevitably, some enhancements to Digital Platform capabilities will require corresponding updates in at least one Digital Service.

Update frequency will depend on the quality of those capabilities, and the amount of central management in your [Paved Road](https://digital-platform.playbook.ee/practices/pave-the-pain-points). The onus is on Digital Platform teams to build high quality platform capabilities that rarely require Digital Service teams to make changes themselves. Low-quality platform capabilities and little central management could mean Digital Service teams have to perform regular updates.

Digital Services updates can be designed as either mandatory migrations, or optional upgrades. Mandatory migrations on short timelines can frustrate Digital Service teams, who will have their own delivery timelines to satisfy. Bi-directional feedback loops and trusted relationships can be sorely tested.

We’ve learned that optional upgrades with longer timelines are less painful for all concerned. The Digital Platform teams need to do as much work as possible without the Digital Service teams. When Digital Service teams need to make changes themselves, it’s the responsibility of the Digital Platform teams to design an optional upgrade framed with compelling benefits for the Digital Service teams. An optional upgrade needs to include a step-by-step upgrade guide, a list of any upgrade dependencies, and a clear offer of assistance.

### Enable You Build It You Run It

Our [accelerate Continuous Delivery and Operability principle](https://digital-platform.playbook.ee/principles#accelerate-continuous-delivery-and-operability) means curated processes on a Digital Platform are clearly opinionated in favour of Continuous Delivery and Operability for all Digital Service teams. 

The production support method of You Build It, You Run It refers to developers supporting their own production services. You Build It You Run It unlocks weekly or more frequent deployments for Digital Service teams, as it eliminates any operational handoffs. It also incentivises Digital Service teams to balance their time between product and operational features. The net result is more frequent production deployments, and more reliable live services. 

A Digital Platform can be used to promote this practice. Digital Platform teams need to create platform capabilities that make it as easy as possible for Digital Service teams to own, build and run their Digital Services without interventions. Digital Service teams will respond positively to the challenge of operating live services. Digital Platform teams only support their own platform capabilities. 

Organisational pressure may exist on a Digital Service or Digital Platform team to increase throughput. Empowering that team to reorganise itself can help it to cope with demand. One option would be to slice the team in two, based on product needs.

