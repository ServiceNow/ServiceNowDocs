---
title: Relish Integration for Supplier Lifecycle Operations
description: The SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\) provides an integration between Relish and Supplier Case Management plugin.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Relish Integration for Supplier Lifecycle Operations

The SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\) provides an integration between Relish and Supplier Case Management plugin.

**Important:** Check your entitlements to determine whether you have access to Relish Integration for Supplier Lifecycle Operations.

Relish is a third-party supplier intelligence platform that helps in validating supplier data while working on supplier cases \(for banking information change requests, supplier location change requests, and conducting sanction screening\). For more information, see [Review supplier information using Relish](review-supp-info-relish.md).

To install SLO Connector for Relish Data Assure, the following plugins have to be installed:

-   **Required plugins**:
    -   SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\)
    -   Relish Data Assure \(x\_reliq\_relish\_dat\)
-   **Dependent plugin**: Source-to-Pay integration framework \(sn\_spend\_intg\)

After SLO Connector for Relish Data Assure is installed, Relish shares the client ID and password. A basic authentication profile must be created using the client ID and password. For more information, see [Set up authentication profile using Relish credentials](../task/auth-profile-using-relish.md).

-   **[Set up authentication profile using Relish credentials](../task/auth-profile-using-relish.md)**  
Create a basic authentication profile that can be used for web service integration with Relish. Register the Relish user name and password to create the authentication profile.

**Parent Topic:**[Integrate Supplier Lifecycle Operations with other applications](integrate-slo.md)

**Related topics**  


[Supplier Lifecycle Operations integration framework](slo-int-framework.md)

[Craft.co Integration for Supplier Lifecycle Operations](craft-integration.md)

[News Integration for Supplier Lifecycle Operations](supp-news-integration.md)

[Set up authentication profile using Relish credentials](../task/auth-profile-using-relish.md)

