---
title: View Configuration Compliance authoritative sources
description: Use this module to view summary information about each authoritative source and to research the source publications that were used to create the record.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuration Compliance reference information, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# View Configuration Compliance authoritative sources

Use this module to view summary information about each authoritative source and to research the source publications that were used to create the record.

## Before you begin

Role required:

-   sn\_vulc.admin to update
-   sn\_vulc.remediation\_owner to view

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Supporting Data** &gt; **Authoritative Sources**.

2.  Click the **Short description** of the authoritative source you want to view.

    |Field|Description|
    |-----|-----------|
    |Number|ID number assigned to the authoritative source by your instance during the import process.|
    |Source|System name of the third-party scanner application, or the name entered in the scanner plugin for the API that communicates with Configuration Compliance.|
    |Source ID|Identifier assigned to the authoritative source by the third-party scanner.|
    |Short description|Name given to this authoritative source in the third-party scanner.|
    |Publisher|Name of the organization or publication that was the original source of information for this authoritative source.|
    |Citations|List of cited information about the test results. Imported from the third-party scanner. You can navigate this list to detailed information about a specific test, if necessary.|

3.  Add a **Publisher**.

4.  Click **Update**.

5.  You can delete this record by clicking **Delete**.

    Removes the record from your instance. If it is still in use in your third-party integration, it returns in the next import


**Parent Topic:**[Configuration Compliance reference information](../reference/cc-reference-info.md)

