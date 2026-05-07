---
title: Extend TNI entity support for duplicated ETLs
description: When Telecom Network Inventory \(TNI\) is enabled, every Configuration Item \(CI\) created by a duplicated ETL must have a corresponding TNI Entity.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Telecom Discovery Builder, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Extend TNI entity support for duplicated ETLs

When Telecom Network Inventory \(TNI\) is enabled, every Configuration Item \(CI\) created by a duplicated ETL must have a corresponding TNI Entity.

## Before you begin

Role required: admin

-   Ensure TNI is installed and active in your instance.
-   Complete the duplication of the Telecom Discovery Builder framework ETL into the target application scope.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub ETL**.

2.  Select the CMDB Application associated with the duplicated ETL.

    The CMDB Integration Studio application in a new page

3.  In the ETL configuration page, check the **Execute Before Script** option.

4.  Replace the default script with the following:

    ```
    (function(input, runId) {
        new sn_tsom_core.TelcoGenericMappingHelper().checkAndUpdateIrePayloadForTni(input);
    })(input, runId);
    ```

5.  Click **Update** to save the changes.

    The duplicated ETL links TNI entities for discovered CIs.


