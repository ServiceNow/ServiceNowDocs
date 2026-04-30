---
title: Domain separation and Insurance claims
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Insurance claims. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2024-09-18"
reading_time_minutes: 3
breadcrumb: [Insurance claims reference, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Domain separation and Insurance claims

Domain separation is supported for Insurance claims. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## How domain separation works in Insurance claims

All [FSO integrations](../../fso-common/concept/fso-overview.md) applications are built on top of and use many Customer Service Management \(CSM\) tables. The key reference tables are the customer tables such as Consumer, Account, and Contact, and these tables are domain-separated.

## Tables

The following tables in Insurance claims are domain-separated:

-   Claim Case \[sn\_ins\_gen\_claim\_case\]
-   Claim Task \[sn\_ins\_gen\_claim\_task\]
-   Claim Adjuster Task \[sn\_ins\_gen\_claim\_adj\_task\]
-   Claim Incident Configuration \[sn\_ins\_claim\_incident\_config\]
-   Itemized Loss/Expense \[sn\_ins\_claim\_incident\_item\]
-   Baggage Incident \[sn\_ins\_claim\_baggage\]
-   Trip Incident \[sn\_ins\_claim\_trip\]
-   Personal Travel Policy \[sn\_bom\_pt\_ins\_policy\]
-   Commercial Travel Policy \[sn\_bom\_ct\_ins\_policy\]

## Use cases

-   **Case Intake**

    The first notice of loss \(FNOL\) intake agents can intake information for an insurance claim on behalf of a customer.

    When the customer calls to file a claim, the intake agent gathers important information that is related to the claim. This can include a description of the incident, itemized losses, and any supporting documentation.

    After collecting the initial details, they open a claim case for a claims specialist to work on.

-   **Claims Analysis**

    A claims specialist works on a claim that they receive through the workspace dashboard.

    The specialist reviews the policy details. If necessary, they can request and review the additional information or documentation from the claimant.

    The specialist sets the reserve funds, modifies the coverage exposures and reserve funds over time, and can also view all activity that is associated with handling the claim.

    The specialist can also make claim approval or denial decisions based on the available evidence.


**Note:** Sometimes a ServiceNow® platform feature or application may be able to effectively support service provider use cases even though the domain framework is not being used. In this case, the application may be assigned Basic\*, Standard\*, or Enhanced\* for its domain support level, and include detailed use cases. For example: Before the New York release, Service Catalog had no domain support. But the instance owner was able to configure separate catalogs and items for each customer in a domain-separated instance. This allowed Service Catalog to be used at a **Standard** support level. To learn more, see domain separation [Application levels of support](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

**Parent Topic:**[Insurance claims reference](insurance-claims-flow-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

