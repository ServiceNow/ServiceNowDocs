---
title: Conduct bulk sanction screening
description: Supplier managers can conduct sanction screening for multiple suppliers simultaneously using the bulk sanction screening feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/perform-bulk-sanction-screening.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 1
keywords: [bulk sanction screening, sanction screening, relish, compliance]
breadcrumb: [Review supplier information using Relish, Manage supplier cases, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Conduct bulk sanction screening

Supplier managers can conduct sanction screening for multiple suppliers simultaneously using the bulk sanction screening feature.

## Before you begin

Ensure that the SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\) is installed. For more information on the required and dependent plugins for Relish, see [Relish Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/relish-slo-connector.md).

Role required: sn\_slm.manager, sn\_slm.owner, or sn\_slm.admin

## About this task

You can check the sanction status of up to 100 suppliers at a time.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Manage Suppliers**.

    **Note:** The **Check sanctions** button appears on the **My suppliers** page only when the Relish plugin is installed and at least one supplier is selected.

2.  Select the suppliers for which you want to conduct sanction screening.

    You can select up to 100 suppliers at a time. If you select more than 100 suppliers, an error message appears.

3.  Select **Check sanctions**.

    The sanction screening process begins. This process can take several minutes depending on the number of suppliers selected.

    After the screening is complete, the Sanction status and Last sanction check date are automatically updated for each supplier.


## Result

The Sanction status field for each supplier is updated with one of the following values:

-   **Clear**: Sanction screening passed or passed with cautions
-   **Blacklisted**: Sanction screening failed
-   **Skipped**: Sanction screening was bypassed or could not be completed

**Parent Topic:**[Review supplier information using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/review-supp-info-relish.md)

**Related topics**  


[Conduct sanction screening](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/conduct-sanction-screening.md)

