---
title: Microsoft SCCM software usage
description: Activate the Microsoft SCCM software usage plugin to integrate your software usage data with the ServiceNow AI Platform.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Microsoft SCCM software usage

Activate the Microsoft SCCM software usage plugin to integrate your software usage data with the ServiceNow AI Platform.

One of the following Microsoft SCCM Software Usage plugins must be installed to import software usage data from Microsoft SCCM to Software Asset Management.

-   Integration — Microsoft SCCM 2012 v2 Software Usage \(com.snc.samp\_usage\_sccm\) plugin
-   Integration — Microsoft SCCM 2016 Software Usage \(com.snc.samp.usage\_sccm\_2016\) plugin

The Integration — Microsoft SCCM 2016 plugin is compatible with SCCM version 1606, 1906, 1910, and 2002.

**Important:** Both Microsoft SCCM plugins will be deprecated in the Tokyo release. If you are integrating with SCCM for the first time, request and install the Service Graph connector for Microsoft SCCM application from the[ServiceNow Store](https://store.servicenow.com/) instead. If you have already activated one of the Microsoft SCCM plugins on your ServiceNow instance, use the Migration Readiness Tool for Service Graph Connector for SCCM store application to prepare your instance for migration from the Microsoft SCCM plugin to the Service Graph connector. See Service Graph connector for Microsoft SCCM for more information on the Service Graph connector.

The SCCM integration plugin installs [several components](../reference/sccm-sam-components.md).

After the SCCM usage plugin is [activated and configured](../task/configure-sccm-sam.md), a scheduled import runs monthly to bring SCCM software usage data into your instance. The usage data is then mapped to Software Usage table. During the scheduled job, a SQL query is executed.

The scheduled import runs once a month, but you can run the import on demand by clearing the **Conditional** option on the Scheduled Data Import form. However, the data is always pulled from the previous month, so there won't be a change in the data until the following scheduled import.

**Note:** The SCCM software usage data source can't be executed directly because the SQL statement doesn't actually pull in the data, so the records aren't retrieved. A valid SQL statement on the data source is updated dynamically though a scheduled import. So, if you need to pull the data into your ServiceNow instance, use the scheduled import.

There are two types of data \(total usage and last used\) that you can extract from SCCM and import into your instance. Last used data will only show the last time the software was used during the previous month.

Total usage data will show down to the second when the software was used in the previous month, which can be a large amount of data imported into your instance. A usage record tracks the sum of usage on a monthly basis so that you can assess the software usage in your environment.

Depending on what you've specified in the reclamation rule for the product, one of the following scheduled imports will run to pull in the data.

-   SAMP Usage Import
-   SAMP Usage 2016 Import
-   SCCM 2012 v2 Software Last Used
-   SCCM 2016 Software Last Used

**Note:** Only usage data for products associated with a reclamation rule is imported. The **Reclamation type** field on the Reclamation Rule form must match the scheduled import that you are running, otherwise the data is not pulled into your instance. For more information, see [Create a reclamation rule to import Microsoft SCCM usage data](../task/create-reclamation-rule-sccm.md).

You can also pull in user data from SCCM. User data is compared to the user\_name field of the sys\_user record. If the names don't match, the user data isn't imported.

**Note:** Configuration item \(CI\), user, product, and publisher values are used to identify a matching software installation.

Duplicate usage information cannot be created for the same CI, user, product, or publisher values in the same month and year.

You can also import usage information using ServiceNow import sets feature.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

