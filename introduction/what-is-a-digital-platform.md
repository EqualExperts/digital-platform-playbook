# What is a Digital Platform

At Equal Experts, we define a **Digital Platform** as follows:

> A Digital Platform is a bespoke Platform as a Service \(PaaS\) product composed of people, processes, and tools, that enables teams to rapidly develop, iterate, and operate Digital Services at scale.

A Digital Platform will allow your organisation to accelerate its time to market, increase revenue, reduce costs, and create innovative products for your customers.

A Digital Platform is:

* _Differentiating_. It empowers your teams to concentrate on solving real business problems by abstracting away organisational complexities and toil.
* _A product._ It’s built incrementally by incorporating feedback from your teams. It accelerates the delivery of Digital Services. It's enduring.
* _Opinionated_. It makes it easy for your teams to build, deploy, and operate Digital Services by providing a curated set of high quality building blocks.

A Digital Platform is also:

* _Not a commodity_. It cannot be bought off the shelf, as it must satisfy the specific needs of your organisation. It’s built by weaving together open-source and bespoke commodity tools to create a technology accelerator.
* _Not a project._ It isn’t a one-off development with a fixed end date. It needs to keep changing, as the needs of your teams will change based on their customers’ demands.
* _Not a universal infrastructure platform_. It cannot run all cloud services for all possible consumers without weakening the proposition. It needs to focus on a subset of cloud services to support Digital Service workloads.

It’s important to remember that a Digital Platform isn’t a silver bullet. It’s a long-term commitment to Digital Services at scale. It’s not appropriate for all workloads, teams, or organisations. For more on this, see [when to start a Digital Platform](https://digital-platform.playbook.ee/introduction/when-to-start-a-digital-platform).

A **Digital Service** is a software service designed to fulfil a product capability and run on a Digital Platform. Such a service might be a monolith, or composed of multiple microservices. It’s usually based on modern software development principles, such as [12 Factor](https://12factor.net/) or [Secure Delivery](https://secure-delivery.playbook.ee/). It's owned by a single Digital Service team responsible for understanding its customers, and producing a service that meets their needs.

Here’s a services diagram of a fictional Digital Platform in a retail organisation. It shows eight Digital Services in development within two different retail domains, as well as six platform capabilities within the Digital Platform itself.

**TODO DIAGRAM**

## Bespoke

A Digital Platform is bespoke. It’s something unique, built solely for the Digital Service teams in your organisation. It’s founded on custom building blocks made by your Digital Platform teams, and commodity cloud services from your public cloud. It’s about peoples, processes, and tools coming together to form platform capabilities. A public cloud can’t provide you with a Digital Platform out of the box. Nor can an off the shelf product from a vendor. 

There are many advantages and opportunities that come with a public cloud as a foundation for a Digital Platform. An [on-premise Digital Platform](https://digital-platform.playbook.ee/pitfalls/on-premise-digital-platform) is a significant pitfall that should be avoided wherever possible.

## Paved Road

A Digital Platform is a set of [Paved Roads](https://www.oreilly.com/library/view/oscon-2017-/9781491976227/video306724.html). Each Paved Road consists of low-friction, hardened interfaces that comprise user journeys for Digital Service teams \(e.g. build a service, deploy a service, or service alerts\). Those paved user journeys are fully automated and encompass the learned best practices specific to your organisation. 

A Paved Road is built incrementally by Digital Platform teams. Each platform capability is delivered in small increments, and adjustments are made based on user feedback. Over time, as each platform capability becomes more opinionated, the Paved Road becomes wider and longer. [Enabling constraints](https://theitriskmanager.com/2018/12/09/constraints-that-enable/) are used to encourage frequent production deployments and high standards of reliability for long-lived Digital Services.

A Paved Road eliminates common failure modes, by automating repetitive tasks. It encourages the adoption of Continuous Delivery and Operability practices, such as constant monitoring of live traffic, and steers away from pitfalls such as [End-To-End Testing](https://digital-platform.playbook.ee/pitfalls/industralised-end-to-end-testing). It challenges Digital Service teams to rethink how they approach particular problems, and contribute enhancements and features back into the Paved Road experience. 

## Bi-directional feedback

A Digital Platform is primarily about the people who build it and use it. It exists to satisfy its users’ needs, through technical or non-technical means. The value of its capabilities is derived from the ability of its Digital Platform teams to talk to and learn from its Digital Service teams. It’s the responsibility of the Digital Platform teams to create an ecosystem of bi-directional feedback loops. User feedback allows Digital Platform teams to better understand which technology building block or organisational process needs to be improved, and industrialised so that all teams can benefit. 

For example, feedback from your Digital Service teams might include complaints about a historical, time-consuming change-approvals process in your organisation owned by an overworked change management team. Your Digital Platform needs to provide an automated deployment pipeline that acts as an automated audit trail. If your Digital Platform teams can present a live audit trail that reduces toil for the change management team, their needs might be met by a streamlined, self-service process, in which Digital Service teams peer-review their own change requests.

{% tabs %}
{% tab title="Experience Report" %}
When we built a Digital Platform at an EMEA payments provider, our Digital Service teams reported the change approvals process was a painful bottleneck. It was a manual process via email, with lots of review and sign-off steps. The process existed to provide security and ensure the organisation maintained its PCI DSS compliance.

We worked with the change management team to understand what was needed to give the same assurance as the manual process. Jira tickets were automatically linked to code changes, and auditing was added to ensure complete traceability for deployments. We even included an automated post-deploy email for change reconciliation. The change management team trusted the new process, and agreed to a much simpler, more traceable change process. The collaboration removed a big source of friction for everyone, without compromising important compliance processes.

![Dave Hewett](../.gitbook/assets/davehewett.png)
{% endtab %}
{% endtabs %}



