---
title: Configuration Settings for ServiceNow Spotlight
description: To use the ServiceNow Spotlight feature, set the configuration settings.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Spotlight feature, Configure, Automation Center, Workflow Data Fabric]
---

# Configuration Settings for ServiceNow Spotlight

To use the ServiceNow Spotlight feature, set the configuration settings.

If ServiceNow Spotlight and Automation Center are installed, you get the following system properties, scheduled job, and Spotlight group:

-   System properties: sn\_ac.use.spotlight.score.for.requests, sn\_ac.use.spotlight.group.for.requests

    For detailed description of the system properties, see [Automation Center properties](../reference/automation-center-properties.md).

-   Scheduled job: **Automation Center: Copy spotlight score into request**

    For detailed description, see [Components installed with Automation Center](../reference/components-installed-with-automation-center.md).

-   Spotlight Group: If ServiceNow Spotlight is enabled, you have the Spotlight group named “Automation request group” with default Spotlight criteria set up.

    ```
    /spotlight_groups.do?sys_id=e037711dc3a11110995486d91840dd03​
    ```

    If you need a different criteria than the default criteria to set your execution priority, then you can customize the criteria to meet your requirements and create a new Spotlight group. For more information, see Create a Spotlight group

    For details about the default Spotlight criteria, see [Default criteria](default-spotlight-criteria.md).


**Parent Topic:**[Working with ServiceNow Spotlight feature](spotlight-ac.md)

