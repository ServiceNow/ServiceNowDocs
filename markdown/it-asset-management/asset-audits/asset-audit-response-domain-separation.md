---
title: Domain separation and Asset Audit Response
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Asset Audit Response. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Asset Audits
classification: asset-audits
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Asset Audit Response, IT Asset Management]
---

# Domain separation and Asset Audit Response

Domain separation is supported for Asset Audit Response. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Overview

Asset Audit Response supports domain-based data separation. This domain separation is available across all Asset Audit Response features and tables.

## How domain separation works in Asset Audit Response

Domain separation in Asset Audit Response does not require any additional setup or configuration.

When managing and completing an audit engagement and corresponding evidence request, ensure that you are using data from the same domain across the Audit Workspace, the Asset Governance Workspace, and either the Software Asset Management or Hardware Asset Management application.

**Note:** If you create an evidence request under a specific domain in the Audit Workspace, the corresponding asset evidence task automatically falls under the same domain in the Asset Governance Workspace.

**Parent Topic:**[Asset Audit Response reference](asset-audit-response-references.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

