---
title: Domain separation and Service Graph Connectors
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Service Graph Connectors. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Service Graph Connectors

Domain separation is supported for Service Graph Connectors. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard\*

The support level is Standard but has some exceptions or special conditions.

-   Includes all aspects of **Basic** level support.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must be able to configure minimum viable product \(MVP\) business logic and data parameters. This configuration is done per tenant, as expected for the specific application.

Sample use case: An Admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## How domain separation works in Service Graph Connectors

Domain separation is supported only for multi-instance Service Graph Connectors.

**Note:** The Identification and Reconciliation Engine \(IRE\) uses strict domain separation in releases prior to San Diego. That is, hierarchical domains are not supported.

You must install the Domain Support - Domain Extensions Installer \(`com.glide.domain.msp_extensions.installer`\) plugin before working with the Service Graph Connectors tables. See [Request domain separation](https://www.servicenow.com/docs/csh?topicname=t_ActivateDomainSeparation&version=latest).

Tables that do not have a Domain \(sys\_domain\) column are not domain-separated. You can add a Domain \(sys\_domain\) column to an existing table. See [Add a domain field to a table](https://servicenow.com/docs/csh?topicname=t_AddADomainFieldToATable.html&version=latest).

**Note:**

-   The import set tables are not domain-separated.
-   Transform histories are not domain-separated.
-   The Key Value \[cmdb\_key\_value\] and Software Instance \[cmdb\_software\_instance\] tables, which are related to the Configuration Management Database \(CMDB\), are not domain-separated.

For more information about domain separation for Service Graph Connectors, see the [Service Graph Connector Domain Separation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1002506) article in the Now Support Knowledge Base.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

