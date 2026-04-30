---
title: Domain separation and Knowledge Management
description: Domain separation is supported in Knowledge Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Knowledge Management

Domain separation is supported in Knowledge Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An Admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Overview

Domain separation works differently at different access levels of an application. In Knowledge Management, data, requester, and fulfiller access to knowledge bases are domain separated.

## How domain separation works in Knowledge Management

In Knowledge Management, the following rules apply:

Data: At the data level of domain separation, data visibility is separated from one domain to another. Knowledge bases, user criteria, articles, categories, article feedback, article versions, article templates, and external sources are domain separated in the base system.

**Note:** The data in one domain cannot be seen in any other domain. For example, if you create a Knowledge Management article in a domain A using an article template which is not in domain A, the article will not be visible in domain A. Similarly, if you create a Knowledge Management article in the global domain using a template that is not in global, the article might not be visible in all the domains.

Requester: Requester activities are supported within tenant domains. Users can search; view; comment; and rate articles of their domain, any child domain, and global domains, if feedback is enabled and the knowledge base settings grant them read access to articles.

-   Users in the global domain can access articles in all the domains if read access is granted at knowledge base and/or article level.
-   Users in the parent domain can access articles in that domain, global, and all its child domains if read access is granted at knowledge base and/or article level.
-   Users in the child domain can access articles in that domain and the global domain if read access is granted at knowledge base and/or article level.

Fulfiller: The application can be used by the Fulfiller within the tenant domains as a tenant domain-owned application. Users are allowed to author articles in knowledge bases of their domain, any child domain, and the global domain if the knowledge base has user criteria set up to grant contribute access.

-   Articles are automatically saved to the user’s current domain when the article is created.

-   If the `glide.knowman.allow_edit_global_articles` system property is enabled, users from a domain other than the global domain can check out and edit global articles. Otherwise, system administrators and users from a domain other than the global domain cannot check out global articles and are shown a warning message to that effect. Depending on their access, users can change their domain to the global domain to check out and edit the global articles.
-   Domains of versioned articles will be maintained as per the latest article version's domain. This includes updating the domain for kb\_version, kb\_knowledge, kb\_feedback, and sys\_attachment tables.
-   If domains contain another domain: If Domain A contains Domain B, users with access to Domain A can author articles in Domain B by toggling the domain scope. To learn more about toggling domain scope, see [Visibility domains and Contains domains](https://www.servicenow.com/docs/access?context=c_DomainVisibility&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

See [Managing access to knowledge bases and knowledge articles](user-access-knowledge.md) to learn how to control contribute and read access to knowledge bases and knowledge articles.

## Use cases

This image demonstrates a basic domain hierarchy that is available in the base system.

![Domain Separation Use Case](../image/DomainHierarchy.png)

## Requester use cases

|User domain|Knowledge base domain|Read user criteria domain|Article domain|Result|
|-----------|---------------------|-------------------------|--------------|------|
|Global|Global|Global|Global|Can view, comment, rate articles.|
|Parent domain \(TOP\)|Parent domain \(TOP\)|Parent domain \(TOP\)|
|Child domain \(TOP/ACME|Child domain \(TOP/ACME|Child domain \(TOP/ACME|
|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|
|Parent domain \(TOP\)|Global|Global|Global|
|Parent domain \(TOP\)|Parent domain \(TOP\)|Parent domain \(TOP\)|
|Child domain \(TOP/ACME|Child domain \(TOP/ACME|Child domain \(TOP/ACME|
|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|
|Child domain \(TOP/ACME\)|Global|Global|Global|Can view, comment, rate articles.|
|Parent domain \(TOP\)|Parent domain \(TOP\)|Parent domain \(TOP\)|
|Child domain \(TOP/ACME|Child domain \(TOP/ACME|Child domain \(TOP/ACME|
|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|

## Fulfiller use cases

|User domain|Knowledge base domain|Contribute user criteria domain|Article domain|Result|
|-----------|---------------------|-------------------------------|--------------|------|
|Global|Global|Global|Global|Can author, update, view, comment, rate articles.|
|Parent domain \(TOP\)|Parent domain \(TOP\)|Parent domain \(TOP\)|
|Child domain \(TOP/ACME|Child domain \(TOP/ACME|Child domain \(TOP/ACME|
|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|
|Parent domain \(TOP\)|Global|Global|Global|
|Parent domain \(TOP\)|Parent domain \(TOP\)|Parent domain \(TOP\)|
|Child domain \(TOP/ACME|Child domain \(TOP/ACME|Child domain \(TOP/ACME|
|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|
|Child domain \(TOP/ACME\)|Global|Global|Global|Can author, update, view, comment, rate articles.|
|Parent domain \(TOP\)|Parent domain \(TOP\)|Parent domain \(TOP\)|
|Child domain \(TOP/ACME|Child domain \(TOP/ACME|Child domain \(TOP/ACME|
|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|MSP domain \(TOP/MSP\)|

## Known Issues

-   The following AQI tables are not domain separated:
    -   AQI Checklist \[kb\_quality\_checklist\]
    -   Checklist Question \[kb\_checklist\_question\]
    -   Article Checklist Answer \[kb\_article\_checklist\_answer\]

        **Note:** The Article Checklist Answer table does not contain the Order field. The application shows the list in a random order.

-   Comment provided by a user on an article is stored in article's domain instead of user domain.

**Parent Topic:**[Knowledge Management reference](../reference/knowledge-management-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

