# When to start a Digital Platform

We’ve established criteria below for starting a Digital Platform. These are the minimum criteria that need to be met, before funding is allocated and development work begins. We recommend you revisit these criteria once a quarter in your first year, and once a year after that. This will help you to understand the target architecture of your Digital Platform, and continuously validate the vision for your Digital Platform.

1. Multi-year funding
2. Homogeneous workload
3. At least one Digital Service team at outset
4. Empowered teams
5. Potential for five Digital Service teams

### Multi-year funding

A Digital Platform is a significant investment. It's a strategic asset rather than a cost-cutting liability. It's funded as a product. 

Multi-year funding is a positive signal of a commitment to continuous improvement. Without that commitment, your Digital Platform teams will not be able to redesign platform capabilities to satisfy changing user needs, or leverage new commodity cloud services to reduce costs.

### Homogeneous workload

A Digital Platform is based on a homogeneous workload, created by multiple Digital Services. If different Digital Services have heterogeneous workloads, your Digital Platform teams will be slower to deliver new features. They will have to seek consensus between different Digital Service teams on which platform capabilities need to be enhanced. The user experience for Digital Service teams will be diminished.

For example, a Digital Platform could support Kotlin microservices and React frontends. A team might ask for data pipelines to be supported as an additional workload type, for a one-off Digital Service. That request would be politely declined by the Digital Platform teams, and there would be a collaborative effort to find an alternative solution outside the Digital Platform. 

### At least one Digital Service team at outset

A Digital Platform starts with a minimum of one Digital Platform team and one Digital Service team. This means the first bi-directional feedback loop can be established between teams, and the initial platform features can be quickly validated. 

Your first Digital Service team needs to have completed its [inception](https://inception.playbook.ee/) phase. This ensures the Digital Service workload is sufficiently well understood to begin construction of the Digital Platform. Otherwise, the delivery of new platform features will be slowed down, due to the rework needed to focus on a different workload type. 

A Digital Platform team that starts out without a Digital Service team will fall into the [Premature Digital Platform Team pitfall](https://digital-platform.playbook.ee/pitfalls/premature-digital-platform-team).

### Empowered Teams

A Digital Platform exists in an ecosystem in which Digital Platform teams are free to make their own technology choices. They need to work independently of any pre-approved tools, so they can experiment with new technologies that meet the particular needs of the Digital Service teams. 

In a similar vein, Digital Service teams have freedom within the Digital Platform ecosystem. The Digital Platform teams build platform capabilities with sensible defaults, and Digital Service teams can configure them as necessary. 

There needs to be some pragmatism. Digital Platform and Digital Service teams need to include pre-existing tools when exploring problems. However, the people best suited to make decisions are those closest to the work, and they must not be beholden to an old list of ill-suited technologies. 

### Potential for five Digital Service teams

A Digital Platform has multi-year funding linked to a recognition that at least five Digital Service teams are likely to exist in the future. In other words, there needs to be sufficient product demand for at least five distinct Digital Services within your organisation. From our experience of building Digital Platforms with multiple organisations, we believe this is the tipping point at which strategically investing in a Digital Platform is beneficial.

If there is zero potential for five or more Digital Service teams, we don’t believe a Digital Platform is the right approach. You won’t achieve the economies of scale to validate the multi-year funding. A better approach would be to invest funding and resources directly into your handful of teams, ensuring they can build and operate their services.

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>
          <img src="https://lh4.googleusercontent.com/fmtSlQF3H8-x3ufYIUft8Y7xYwiOdSFcqS8hR9qKXLlQPTo7rjEOdEW4B1XANjf0hwX750wOJQYxtJiTz8y5KYoV377ZF_eYjPm3vRQiu4bzRgn1hyQQmnE5eBiPNnvbfb9Ncsoq"
          alt/>
        </p>
      </td>
      <td style="text-align:left">
        <p>O2 Priority is a popular customer loyalty service, and in 2016, it lacked
          the operational capacity to meet demand. I joined the team with the primary
          goal of building a new scalable platform. We used many of the practices
          mentioned in this playbook, but it wasn&#x2019;t a full-blown Digital Platform
          as described because we only had one service team.</p>
        <p></p>
        <p>Work happened in phases, including automated infrastructure with observability
          built in, and automated deployment pipelines. These capabilities set the
          foundation for seamless migration of O2 Priority. The service team went
          from a deployment frequency of fortnightly to daily, and from an MTTR of
          days to three hours.</p>
        <p></p>
        <p>Looking back, I believe our success was due to:</p>
        <p></p>
        <ul>
          <li>commitment and support from our primary stakeholders</li>
          <li>autonomy to build and run the scalable platform using the best tools and
            technologies available</li>
          <li>feedback from the service team and building to their requirements</li>
          <li>investing in observability and telemetry dashboards</li>
        </ul>
        <p>The benefit to O2 was significant &#x2013; they increased their ability
          to create and run loyalty campaigns better targeted to their customers.&#x201D;</p>
        <p></p>
        <p> <a href="https://www.linkedin.com/in/ogonnaiwunze/">Ogonna Iwunze</a>,
          Operability Engineer</p>
      </td>
    </tr>
  </tbody>
</table>

