---
title: Evaluating the need for domain separation
description: You may find that domain separation doesn't always work for your customers' organizations. It's best that you base your decision to go with domain separation by looking at your customers' needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-evaluation-dom-sep.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Evaluating the need for domain separation

You may find that domain separation doesn't always work for your customers' organizations. It's best that you base your decision to go with domain separation by looking at your customers' needs.



## Reasons for domain separation

These factors may help you decide to choose domain separation for your customers' organizations:

-   Your customers have moderate alignment of processes and general platform requirements.
-   Your customers plan to work on tasks as fulfillers rather than as requesters.
-   Your customers have a contractual agreement that requires that data records be isolated, but your instance owner has determined that the requirement may be addressed somewhere else in the configuration.
-   Your company's instance owners have entire entities that operate as physically separate organizations and do not share data, but full reporting is still required. Separate domains would allow data visibility when configured correctly.

## Reasons for no domain separation

These factors can point to reasons why your customers' organizations might not want to set up domain separation:

-   Your customers want to administer their environment, have full ownership of it, and set the roadmap for expansion.
-   Your customers require that the data and process at the physical or database level be completely isolated.

    **Note:**

    Domain-separated instances contain a shared database so this undermines the isolation requirement.

-   Departments in your customers' organization want to isolate records. \(Access controls may suffice.\)
-   Your customers all want their own processes, business rules, and workflows.
-   The corporate culture is one of non-collaboration between your customers' organizations.
-   Your customers interact with the platform as end users only.

\[Omitted image "bp-evaluating-need.png"\] Alt text: Evaluating reasons for and against choosing domain separation

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained]()

[Domain separation hierarchies]()

[Context and domain separation]()

[Segregating and securing data with domain separation]()

[Alternatives to domain separation]()

[Benefits of domain separation]()

[How a database query works with domain separation]()

[Domain separation levels of support]()

[Service provider reference architecture]()

[Domain separation terms]()

[Domain-separate a custom table]()

[Customizing domain properties and themes]()

[Managing domain separation for specific uses]()

[Configuring domain separation with the domain picker]()

[Domain separation performance considerations]()

[Setting up domain hierarchies]()

[Checking domain logs for errors and warnings]()

[Importance of the Default domain]()

[Contains queries and domain access]()

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()

