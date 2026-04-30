---
title: Domain separation and Threat Intelligence Security Center
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.Domain separation is supported for Threat Intelligence Security Center. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Reference, Threat Intelligence Security Center, Security Operations]
---

# Domain separation and Threat Intelligence Security Center

Domain separation is supported for Threat Intelligence Security Center. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Overview

Domain separation is enabled for all the features of Threat Intelligence Security Center.

## How domain separation works in Threat Intelligence Security Center

-   All the configuration related records that are provisioned in the base system are shipped in the global domain. In case the instance is domain separated, users would see an explicit button **Setup TISC** under the **Administration** module of the TISC workspace. Click on this button to clone the base system provisioned global domain configurations into the respective domains.

    ![TISC Domain Separation](../image/tisc-domain-separation.png "Domain Separation")

    **Note:** Users should only enable or modify domain specific configuration records and should not enable or modify configuration records in the global domain.

-   Couple of platform notification rules \(sysevent\_email\_action\) are provisioned in the base system, these notification rules should be cloned into required domains and only domain specific notification rules need to be enabled.

    **Note:** For more information on the rules notifications, navigat to **System Notification** &gt; **Notifications** and filter for all the global domain notification rules defined on the tables starting with name sn\_sec\_tisc to understand how users can identify the base notification rules that are provisioned in the base system.

-   All the configurations and data ingested will be specific to each domain, which means that users from one domain will not be able to access data from other domain.
-   Configure a domain-separated environment with this application by installing Domain Support - Domain Extensions Installer plugin.
-   There are domain columns added for all the base system application tables.
-   Using the Platform provided functionality the tenant domains manage their own application data.
-   The business logic and processes that can be domain-separated by instance owner is same as what Platform supports.
-   The business logic and processes that can be administered by tenant domain is same as what platform supports.
-   You can access the Setup page from the Administration section. Click on the link provided under the Administration section to view the domain separation view.
-   To support the domain separation for the widgets using Performance Analytics \(PA\) indicators in the TISC Home dashboard, refer to the KB article [KB1647990](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=5a53149d97070654f03d739c1253afbb) for detailed procedure.

## Domain Separated tables

All the tables are domain separated.

## Use cases

All features of this application are domain separated.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

