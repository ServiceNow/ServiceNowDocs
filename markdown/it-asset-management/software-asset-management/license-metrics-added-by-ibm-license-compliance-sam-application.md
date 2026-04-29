---
title: License metrics added by the IBM License Compliance for Software Asset Management application
description: The IBM License Compliance for Software Asset Management application adds license metrics that enable you to classify your IBM software products.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Request the IBM License Compliance for Software Asset Management application, Setting up an ASP integration, Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# License metrics added by the IBM License Compliance for Software Asset Management application

The IBM License Compliance for Software Asset Management application adds license metrics that enable you to classify your IBM software products.

These additional license metrics are available only if you have activated the Software Asset Management publisher pack for IBM and installed the IBM License Compliance for Software Asset Management application. They are not available if you have only activated the Software Asset Management publisher pack for IBM.

You can also use license metrics to reconcile the software products that are discovered in your environment. The Software Asset Management application automatically adds [default license metrics](../concept/c_SAMLicenseMetrics.md) for supported software publishers by using publisher-specific metric groups, such as the Adobe and Microsoft metric groups. These license metrics are then set in your corresponding software entitlements and used for reconciliation. Any additional license metric that is not included in an existing metric group must be added as a custom license metric in order to be used for reconciliation. Custom license metrics modify the reconciliation process by adding software license calculations that are not already included in the default list of supported license metrics.

By default, the IBM metric group includes the following license metrics for IBM reconciliation:

-   Authorized User
-   Authorized User Value Unit
-   Employee User Value Unit
-   External User Value Unit
-   Per Device
-   Per Named User
-   Per Processor \(CPU count\)
-   Per user
-   Processor Value Unit \(PVU\)
-   Resource Value Unit \(RVU\)
-   Virtual Processor Core \(VPC\)

All other license metrics that are added by the IBM License Compliance for Software Asset Management application are not included in the IBM metric group. If you want to reconcile your IBM software products using any of these license metrics, you must create a corresponding custom license metric on your ServiceNow instance. See [Add a custom license metric](../task/add-custom-license-metric.md) for more information on how to create a custom license metric.

**Parent Topic:**[Request the IBM License Compliance for Software Asset Management application for Authorized Software Asset Management Provider \(ASP\) integrations](../task/request-ibm-license-compliance-sam-application.md)

