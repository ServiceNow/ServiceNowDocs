---
title: Enabling access to a data source
description: Work with your data source administrator to enable access to your external data source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/enabling-access-data-source-zcc.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Zero Copy Connectors, Workflow Data Fabric]
---

# Enabling access to a data source

Work with your data source administrator to enable access to your external data source.

To connect to a data source behind a private network using a zero copy connection, there are two general approaches:

-   **IP allowlist**

    Your data source admin must allow access to a source IP range based on where the zero copy queries are coming from. For help with identifying the correct IP range, contact your account manager or Customer Service and Support and reference KB1706533. If you're unable to access the KB article and need immediate assistance, use one of the contact numbers from our [support contact page](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1000420).

-   **Private connectivity**

    For data sources hosted behind private Virtual Private Clouds \(VPCs\) or Virtual Networks \(VNets\) in the public cloud, connectivity options are available that enable query traffic to transit over private IP address space, end to end. This private connectivity is enabled by technologies such as [Private Link](https://learn.microsoft.com/en-us/azure/private-link/private-link-overview). Each cloud provider implements this technology differently. To explore private connectivity options for your specific topology, contact your account manager or Customer Service and Support.


**Parent Topic:**[Configuring Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configuring-zcc.md)

