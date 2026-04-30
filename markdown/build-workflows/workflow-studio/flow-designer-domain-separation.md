---
title: Domain separation and Workflow Studio
description: Domain separation is supported in Workflow Studio. Workflow Studio supports domain separation of business logic, which lets each tenant domain have its own flows, actions, and subflows. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-02-12"
reading_time_minutes: 5
breadcrumb: [Exploring flows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Domain separation and Workflow Studio

Domain separation is supported in Workflow Studio. Workflow Studio supports domain separation of business logic, which lets each tenant domain have its own flows, actions, and subflows. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard\*

-   Includes **Basic** level
-   Business logic: Processes can be created or modified per customer by the service provider. The use cases reflect proper use of the application by multiple service provider customers in a single instance.
-   The owner of the instance needs to be able to configure MVP business logic and data parameters per tenant as expected for the specific application.

Use case: As an admin, I need the ability to make comments mandatory on close of a record for one tenant, but not for another.

## How domain separation works in Workflow Studio

The system domain separates Workflow Studio content according to these rules.

-   **Workflow Studio content inherits the domain of the user who creates them**

    Flows, actions, and subflows belong to the domain of the user who creates them. For example, when a service provider \(SP\) administrator in the TOP domain creates a flow, it belongs to the TOP domain.

    **Note:** The domain selected from the domain picker overrides the domain the user belongs to. For example, when an SP administrator in the TOP domain selects the ACME domain from the domain picker, any content created belongs to the ACME domain.

-   **Workflow Studio content runs from the domain from which it is triggered or initiated**

    Flows, actions, and subflows run from the domain of the record or user who initiates them. For example, when a user from the child domain ACME triggers a flow belonging to the parent domain TOP, the flow runs in the context of the child domain ACME.

    |Trigger type|Domain assignment|
    |------------|-----------------|
    |API call|Domain of the user making API call|
    |Email trigger|Domain of the email sender|
    |Record trigger|Domain of the triggering record|
    |Scheduled trigger|Domain of the flow|
    |Service Catalog trigger|Domain of the requested item record|

-   **Workflow Studio only runs content accessible from the current domain context**

    The system can only run content to which the current domain context allows access. See [Understanding domain separation](https://www.servicenow.com/docs/access?context=c_DomainSeparation&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) to understand data separation and the domain hierarchy. For example, a user in the child domain ACME can trigger flows belonging to the parent domain TOP, but cannot trigger flows belonging to a sibling domain such as INITECH.

    Workflow Studio runs record operations from the current user domain context. A read operation such as the Lookup Records action returns records based on the currently selected domain and its children. For example, if the currently selected domain is the TOP domain, you will see records from the TOP domain and all its children such as the ACME and INITECH domains. If the currently selected domain is the ACME domain, you will see records from the ACME domain and its children, but you will not see records from the parent TOP domain.

    **Note:** Record operations use the data or process separation rules applied to the table the record belongs to. For example, suppose you have process-separated the Business Rule table. If you add a business rule to the TOP domain, the business rule will be accessible to record operations in child domains such as the ACME domain because process separation allows access to records from parent domains.

    Flows that call another application such as a decision table or workflow also run from the current user domain context.

-   **Workflow Studio runs all flows whose trigger conditions are met**

    A flow in one domain cannot override or prevent a flow from another domain from running. Workflow Studio runs any flow that is visible to the current user and whose trigger conditions have been met. For example, a flow belonging to the TOP domain that is triggered by the creation of an incident record runs anytime an incident is created, regardless of whether the incident is created in the ACME or INITECH child domains.


## General guidelines

Follow these general guidelines when using domain separation with Workflow Studio.

-   **Ensure that tenant flows, actions, and subflows are run properly for domains**

    Since tenants cannot override Workflow Studio content, a service provider \(SP\) administrator from the TOP domain must author and manage them to ensure they run properly for domains. While you can create domain-specific flows, users working from domains higher in the hierarchy may trigger multiple child domain flows. For example, a user working in the TOP domain can trigger flows in child domains such as ACME and INITECH.

    **Note:** Flow authors can see only Workflow Studio content available from their current domain and any parent domains in the hierarchy. Workflow Studio does not display content visible from Contains domains.

-   **Provide a unique name for each flow, action, and subflow**

    Since all domains share Workflow Studio content, have an SP administrator in the TOP domain uniquely name each flow, action, and subflow to ensure that a flow intended for one domain does not duplicate the name of a flow in another domain. For example, add the domain to the flow name such as `Validate incidents - TOP`, `Validate incidents - ACME`, and `Validate incidents - INITECH`.

-   **Ensure that flows and actions only contain artifacts from current or parent domains**

    Workflow Studio prevents the activation of any flow containing artifacts unavailable to the current or parent domains. For example, if you create a domain-specific flow that belongs to the ACME domain, it cannot contain actions or subflows belonging to the sibling domain INITECH.

-   **Edit Workflow Studio content in the domain to which it belongs**

    Users in a parent domain can't see flows, actions, and subflows in a child domain. They must change to the domain to which they belong to edit them. For example, an administrator in the TOP domain can't see flows from the ACME domain. The administrator must switch to the ACME domain to see and edit them.


-   **[Generate group approvals for domain separated requests](../task/generate-group-approvals-domain.md)**  
Configure Workflow Studio to generate approvals for all members of a group or to restrict approvals to only group members who are visible from the domain of the request.

**Parent Topic:**[Exploring flows](../../workflow-studio/concept/exploring-flows.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

