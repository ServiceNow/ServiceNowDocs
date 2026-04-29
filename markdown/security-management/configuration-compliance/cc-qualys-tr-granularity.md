---
title: Configure Qualys Test Result Granularity
description: Configure the Qualys test result granularity to ensure the system imports results at a more detailed level based on your selected configuration keys. In addition to the default keys, you can configure additional keys based on your requirements to increase granularity. Granular imports allow teams to manage their respective assets independently and prevent data from being overwritten when multiple records share common identifiers.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Qualys, Integrate with other applications, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configure Qualys Test Result Granularity

Configure the Qualys test result granularity to ensure the system imports results at a more detailed level based on your selected configuration keys. In addition to the default keys, you can configure additional keys based on your requirements to increase granularity. Granular imports allow teams to manage their respective assets independently and prevent data from being overwritten when multiple records share common identifiers.

## Before you begin

Role required:

-   sn\_vulc.admin

## Procedure

1.  Navigate to **All** &gt; **Configure Qualys Test Result Granularity**.

2.  In the Key Configuration form, confirm that:

    -   **Source integration** is `Qualys Cloud Platform`.
    -   **Table** is set to `Test Result`.
3.  In the **Configuration Key** section, choose the field for which you want to create unique test results.

    For example, selecting **instance** creates unique test results for each instance within a database.

    **Note:** Use this feature with caution. Each additional configuration key increases integration time. To maintain optimal performance, limit your use to no more than three extra keys.

4.  Enter true next to **instance** to enable granularity, or false to disable it.

5.  Select **Update** to save your changes.


