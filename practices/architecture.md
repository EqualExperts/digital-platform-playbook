# Architecture

### Maximise managed services

Push the commodity cloud services within your platform capabilities into your public cloud provider wherever possible. Treating your public cloud provider as Software as a Service \(SaaS\) not Infrastructure as a Service \(IaaS\) allows your Digital Platform teams to transfer more operational responsibilities, freeing time up for them to focus on higher value activities.

Using managed cloud services for commodities such as databases and messaging queues equates to outsourcing your operating costs to a low-cost, highly experienced supplier. It results in easier cloud service upgrades, faster security patching, lower recruitment costs, and higher availability for your Digital Platform. 

Maximising managed services can create lock-in anxiety. It’s important to prioritise business agility and Total Cost of Ownership \(TCO\) over lock-in. Lock-in is only a significant problem when a cloud service is a common utility function with a high switching cost, such as a proprietary Oracle RDBMS in the cloud. Alternative cloud services exist with lower switching costs, such as AWS Aurora. 

### Multi-zone in a single region by default

The architecture of your Digital Platform needs to be predicated on the availability needs of your Digital Services . In [Site Reliability Engineering](https://landing.google.com/sre/sre-book/chapters/embracing-risk/), Betsy Beyer et al describe reliability as a range from 99.0% to 99.999%, and state an additional nine of reliability requires an order of magnitude more engineering effort. We’ve confirmed this insight with multiple clients. 

Your cloud provider will offer cloud services in regions and zones. A region is a large geographic location. It will consist of multiple logically isolated zones, which host cloud services and are usually physically isolated from one another. We recommend multi-zone single region for your Digital Platform architecture in nearly all scenarios. 

Multi-zone single region will provide an effective balance between Digital Platform reliability and engineering effort for many organisations. Multi-zone usually provides geographic redundancies within a single region, and protects your Digital Platform from zonal failures caused by issues such as power outages. 

It’s important to understand the unique availability characteristics of your cloud provider. Each cloud provider will have a majority of its cloud services per-zone, but some will be per-region. In addition, zones and regions may not behave as expected. For example, as of September 2020, the [zones in a GCP region do not have geographic isolation](https://cloud.google.com/compute/docs/regions-zones). This means AWS and Azure have geographic redundancies within a single region, but GCP does not. It might make multi-region service more compelling if your cloud provider is GCP.

### Multi-zone multi-region in some scenarios

Multi-zone multi-region is justifiable when you’re concerned about:

* The availability of cloud commodity services provided by a single region
* Geographically distributed customers experiencing higher latencies, the further they are from your single region
* The time to restore your Digital Platform when your single region fails

Cloud providers currently provide limited support for natively running workloads across multiple regions. The extra complexity added by your bespoke tooling may reduce your overall availability, even as it protects against a single region failure. Some failure scenarios are not improved by multi-region, such as a faulty global rollout of a cloud commodity service. 

We don’t recommend multi-cloud i.e. replicating an entire Digital Platform ecosystem across two different cloud providers. This will force your Digital Platform to use the lowest common denominator of cloud services, and limit reliability to the least reliable cloud provider. Corey Quinn has written a comprehensive explanation of why [multi-cloud is the worst practice](https://www.lastweekinaws.com/blog/multi-cloud-is-the-worst-practice/).

### Name for discoverability

As a Digital Platform ecosystem expands, discoverability becomes crucial. A Digital Service team may need to quickly identify a failing downstream Digital Service, and notify the owning team of the failure. A Digital Platform team may need the ability to locate all Digital Service teams in a particular delivery centre, or all Digital Services with abnormal reliability trends.

Arbitrary naming conventions for Digital Service teams and Digital Services can be actively hostile to new team members. It can be extraordinarily difficult for Digital Service teams to collaborate with one another, and rapidly locate the right person at the right moment. 

Discoverability can be achieved by ensuring a convention by default is used throughout the entire Digital Platform, in all tools and processes. We recommend the following convention:

* all Digital Services are named after the product capability they represent
* all Digital Service teams are named after the Digital Services they’re building

For example, if there is a Digital Service for customer recommendations, both the service and the team need to be named “Customer Recommendations”.

