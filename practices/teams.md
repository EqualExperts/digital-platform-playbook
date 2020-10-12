# Teams

### Prime Digital Platform teams for success

It’s important that Digital Platform teams are set up for success like any Digital Service team. We recommend the following roles for a new Digital Platform team:

* A product manager. Works across the organisation, talks to potential users to win hearts and minds, and drives the direction of the Digital Platform. Experience in product development and experimentation is more important than a technical background.
* A delivery lead. Steers team ways of working and encourages a culture of learning and experimentation.
* A technical analyst. Helps the team to slice and dice work items into appropriate sizes.
* 3 x platform engineers. Develop platform capabilities, foster bi-directional feedback loops with Digital Service teams, and provide advice on how to use the Digital Platform.

This is a recommendation, not a rule. You might need to start out with a smaller team for funding reasons. In that situation, a single person could fill the product manager and delivery lead roles, or delivery lead and technical analyst. It’s important such an accommodation is time limited, to guard against burnout.

### Expand Digital Platform teams

We’ve found the number of Digital Platform teams and their team members needs to gradually increase, as the number of Digital Services increases. We recommend increasing the number of platform engineers, and splitting the Digital Platform team, when you have at least five Digital Service teams. We advocate a division of Digital Platform teams based on your platform capabilities, based on which of them need the most investment at that time. 

We also suggest the following team roles:

* An architect. Steers technology choices, and teaches Digital Service teams how to steer those choices for themselves.
* A tech writer. Creates consistent, coherent documentation guides for Digital Service teams. 
* A user researcher. Helps Digital Platform teams create user personas for Digital Service team members, and steers user experience interviews.

These additional roles might be combined with some platform engineers into a Platform Enablement team, dedicated to accelerating Continuous Delivery and Operability across the Digital Service teams via productivity tooling. Alternatively, these roles might be folded into existing Digital Platform teams.

Scale Digital Platform teams based on platform capabilities and the amount of bi-directional feedback loops with Digital Service teams. This increased cost for the Digital Platform must be included in funding discussions, in order to avoid a loss in utility of the Digital Platform.

For example, a Digital Platform team with a product manager, a delivery lead, a technical analyst, and three engineers. As the number of Digital Services grows, an architect and two more engineers are added. At that point, the delivery lead decides the teams need to split. The product manager decides cloud infrastructure and telemetry are the priorities for the next three months, so those are the two new Digital Platform teams.

### Whole Digital Platform funding

Funding for the Digital Platform needs to be continuous, multi-year, and come from a single budget holder accountable for Digital Platform success. 

The two most common Digital Platform expenses are team costs \(team member salaries\) and cloud provider costs \(e.g. AWS EKS bill\). We’ve seen situations where those costs are paid from two different budgets, which causes unnecessary complications:

* Part-funding of some Digital Platform team members by other operational teams increases key person dependencies
* Part-funding of some Digital Platform teams by a particular Digital Service team reduces product manager accountabilities and causes prioritisation conflicts
* Part-funding of all Digital Platform teams by a particular Digital Service team jeopardises Digital Platform independence and creates warped incentives 

Ideally, the single budget holder is the Digital Platform product manager, as a peer of Digital Service product managers.

{% tabs %}
{% tab title="EMEA payments provider example" %}
At an EMEA payments provider, we started with a Payment Gateway service, with the vision of building a Digital Platform to host and provide other payment services. We invested time in building telemetry tools, which were embedded into the Digital Platform itself.

Within a year, we had a Digital Platform where developers were able to roll out new Digital Services services with minimal help from the Digital Platform team. Newly onboarded teams were able to launch new payment services into production in less than a week. 

These practices helped us:  


* Strong deployment pipelines encouraged teams to deploy frequently.
* Deployment dashboards helped teams get feedback on their deployment frequency.
* Embedded telemetry meant teams could debug and analyse payment abnormalities within the Digital Platform or external integration partners within minutes
* Deep integration of incident management tools into Slack reduced context switching and helped teams to collaborate.
* Feature toggle based development ensured teams kept deploying services that were decoupled from business processes

![Anant Pal](../.gitbook/assets/anantpal.jpeg)
{% endtab %}
{% endtabs %}

