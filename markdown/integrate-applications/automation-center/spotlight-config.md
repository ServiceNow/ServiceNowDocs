---
title: Configuration Settings for ServiceNow Spotlight
description: To use the ServiceNow Spotlight feature, set the configuration settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/automation-center/spotlight-config.html
release: zurich
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with ServiceNow Spotlight feature, Configure, Automation Center, Workflow Data Fabric]
---

# Configuration Settings for ServiceNow Spotlight

To use the ServiceNow Spotlight feature, set the configuration settings.

If ServiceNow Spotlight and Automation Center are installed, you get the following system properties, scheduled job, and Spotlight group:

-   System properties: sn\_ac.use.spotlight.score.for.requests, sn\_ac.use.spotlight.group.for.requests

    For detailed description of the system properties, see [Automation Center properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/automation-center-properties.md).

-   Scheduled job: **Automation Center: Copy spotlight score into request**

    For detailed description, see [Components installed with Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/components-installed-with-automation-center.md).

-   Spotlight Group: If ServiceNow Spotlight is enabled, you have the Spotlight group named “Automation request group” with default Spotlight criteria set up.

    ```
    /spotlight_groups.do?sys_id=e037711dc3a11110995486d91840dd03​
    ```

    If you need a different criteria than the default criteria to set your execution priority, then you can customize the criteria to meet your requirements and create a new Spotlight group. For more information, see Create a Spotlight group

    For details about the default Spotlight criteria, see [Default ServiceNow Spotlight Criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/default-spotlight-criteria.md).


**Parent Topic:**[Working with ServiceNow Spotlight feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/spotlight-ac.md)

