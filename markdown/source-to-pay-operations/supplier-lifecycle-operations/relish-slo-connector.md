---
title: Relish Integration for Supplier Lifecycle Operations
description: The SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\) provides an integration between Relish and the Supplier Case Management plugin.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplier-lifecycle-operations/relish-slo-connector.html
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Relish Integration for Supplier Lifecycle Operations

The SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\) provides an integration between Relish and the Supplier Case Management plugin.

**Important:** Check your entitlements to determine whether you have access to Relish Integration for Supplier Lifecycle Operations.

Relish is a third-party supplier intelligence platform that helps in validating supplier data while working on supplier cases \(for banking information change requests, supplier location change requests, and conducting sanction screening\). For more information, see [Review supplier information using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/review-supp-info-relish.md).

To install SLO Connector for Relish Data Assure, the following plugins must be installed:

-   **Required plugins**:
    -   SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\)
    -   Relish Data Assure \(x\_reliq\_relish\_dat\)
-   **Dependent plugins**:
    -   Source-to-Pay integration framework \(sn\_spend\_intg\)
    -   Supplier Operations \(com.snc.sn\_so\)

After SLO Connector for Relish Data Assure is installed, Relish shares the client ID and password. A basic authentication profile must be created using the client ID and password. For more information, see [Set up authentication profile using Relish credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/auth-profile-using-relish.md).

-   **[Set up authentication profile using Relish credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/auth-profile-using-relish.md)**  
Set up a basic authentication profile using Relish credentials to enable web service integration.

**Parent Topic:**[Integrate Supplier Lifecycle Operations with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/integrate-slo.md)

**Related topics**  


[Supplier Lifecycle Operations integration framework]()

[Craft.co Integration for Supplier Lifecycle Operations]()

[News Integration for Supplier Lifecycle Operations]()

[Set up authentication profile using Relish credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/auth-profile-using-relish.md)

