---
title: Domain separation and Playbooks
description: Data separation is supported for Playbooks. The domain value of the triggering input record determines the domain context. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring playbooks, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Domain separation and Playbooks

Data separation is supported for Playbooks. The domain value of the triggering input record determines the domain context. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## How domain separation works for Playbooks

The system domain separates Playbooks content according to these rules:

-   **Playbooks content runs from the domain it is triggered from**

    Activities and Playbooks run from the domain of the record or user who initiates them. For example, when a user from the child domain ACME triggers a playbook belonging to the parent domain TOP, the playbook runs in the context of the child domain ACME.

-   **Workflow Studio content runs in the domain of the calling Playbooks activity**

    Whenever an activity definition calls an action or flow, the system runs the Workflow Studio content in the same domain context as the triggering Playbooks content. If the Workflow Studio content has a matching domain-specific process override, then the system runs the override version instead. While Playbooks does not support process overrides, it uses any process overrides defined within Workflow Studio.

    **Note:**

    -   A process override refers to a type of [override](https://www.servicenow.com/docs/access?context=domain-sep-override-viewer&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) in domain separation.
    -   Service providers \(SPs\) can use [domain separation](https://www.servicenow.com/docs/access?context=c_DomainSeparation&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), to logically separate data, processes, and administrative tasks into defined groups.
-   **Playbooks configuration files are visible to all domain users**

    Playbooks configuration files are not domain separated. Any user with the appropriate roles can view all playbooks, trigger definitions, and activity definitions.


**Parent Topic:**[Exploring playbooks](process-automation-designer.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

