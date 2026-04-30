---
title: Customer Service Management considerations
description: Consider these points while implementing the CSDM framework.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Customer Service Management and the CSDM guidelines, Getting started with Customer Service Management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Customer Service Management considerations

Consider these points while implementing the CSDM framework.

## Considerations

-   What is a Service-aware Install Base?

    A Service-aware Install Base enables companies to track the digital products and services in use. A Service-aware Install Base also tracks the relationships of the products and services to dependent services and CIs that affect their health.

-   What are Proactive Customer Service Operations?

    Proactive Customer Service Operations bring CSM and Event Management together to enable companies to proactively trigger case workflows and notify the affected customers.

-   Do I must purchase CSM Professional package to use the Service-aware Install Base?

    No. The Service-aware Install Base is included in the CSM base system.

-   Can multiple sold products reference the same service offering?

    Yes. Multiple sold products \(that is, Service Models\) purchased by different companies can reference the same service offering. For example, multiple customers can purchase the same SaaS offering with the same service commitments.

-   Can multiple Install Base Items reference the same application service?

    Yes. Multiple Install Base Items \(either for the same account or for different accounts\) can reference the same application service. For example, a multi-tenant SaaS offering where multiple customers \(each with their own Install Base Item\) are used on the same production instance \(application service\).

-   When do I create an incident rather than a proactive case from an alert?

    Typically, some companies create an incident so that their NOC engineers can resolving the issue. After they determine that the issue impacts multiple customers, they also proactively create a major case and related child cases \(one for each impacted customer\) to notify the affected customers. Thus, the alert, incident, and case are all linked.

    Updates made by the resolving teams to the incident status or additional comments are reflected in the case. The customer service teams use these updates to keep customers informed.

    To meet the customer notification time requirements of the SLAs, companies may also automate creating incidents and cases from the alert. In addition, companies can also create a proactive case from the alert while the issue is being resolved.

-   What is the difference between entitlements managed at the CSDM Service Offering and the CSM Contracts and Entitlements?

    Service Commitments in CSDM define the expected level of a service. A service offering consists of a set of service commitments which uniquely define the service offerings. For example, a service offering may include a service commitment to perform a data backup each night.

    Service contracts in CSM store information about the type of support that is provided to a customer. A contract can include an account or consumer, a contact, and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs. An entitlement defines the type of support that a customer receives, as well as the supported communication channels. For example, a customer may sign a service contract to receive support from 6:00 a.m. to 9:00 p.m. on weekdays.

-   How can I request additional services based on the product that I've purchased?

    The relationship between the product model and the catalog items enables you to use the customer portal to request additional services for the products you've purchased. Multiple catalog items can be associated with a product model.

-   Do I need elements from all the CSDM domains to set up CSM?

    No. The approach mentioned in this use case is based on the recommended guidelines and assumes you are in the Run or Fly stage of the CSDM implementation. See [Implementing the CSDM framework in stages](https://www.servicenow.com/docs/access?context=csdm-implementation-stages&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

    When you’re implementing CSM, start with the tables in the CSDM Foundation domain and the CSM Customer Service domain. Using these domains enables you to leverage the capabilities included in CSM.

    To enable the proactive customer service operations, use tables from the CSDM Manage Technical Services domain for monitoring the application services tied to the customers’ install base. Using this domain enables you to leverage the CSM and ITOM integration.

    Service-centric organizations can leverage the tables from the CSDM Sell/Consume domain to connect the product model to the service offerings and then to sold product. These connections enable you to track the service portfolio and see a complete view of how customers are consuming services.


