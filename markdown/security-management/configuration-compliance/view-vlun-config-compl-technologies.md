---
title: View Configuration Compliance technologies
description: Use this module to view summary information about each authoritative sources and citation \(also known, in Qualys, as a framework\). You can research the source publications that were used to create the record.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuration Compliance reference information, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# View Configuration Compliance technologies

Use this module to view summary information about each authoritative sources and citation \(also known, in Qualys, as a framework\). You can research the source publications that were used to create the record.

## Before you begin

Role required:

-   sn\_vulc.admin to update
-   sn\_vulc.remediation\_owner to view

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Supporting Data** &gt; **Technologies**.

2.  Click the **Short description** of the authoritative source you want to view.

    |Field|Description|
    |-----|-----------|
    |Number|ID number assigned to the authoritative source by your instance during the import process.|
    |Source|System name of the third-party scanner, or the name entered in the third-party scanner plugin for the API that communicates with Configuration Compliance.|
    |Source ID|Identifier assigned to the authoritative source by the third-party scanner.|

3.  You can delete this record by clicking **Delete**.

    Removes the record from your instance. If it is still in use in your third-party integration, it returns in the next import


**Parent Topic:**[Configuration Compliance reference information](../reference/cc-reference-info.md)

