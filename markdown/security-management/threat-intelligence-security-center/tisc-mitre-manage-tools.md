---
title: Manage Tools
description: Manage the tools information that you imported from the MITRE TAXII collections. Tools are legitimate software that are used by threat actors to perform attacks.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [MITRE-ATT&amp;CK Repository, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Manage Tools

Manage the tools information that you imported from the MITRE TAXII collections. Tools are legitimate software that are used by threat actors to perform attacks.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

Tools enable you to know how and when threat actors use them for executing campaigns. Unlike malware, these tools or software packages are often found on a system and have legitimate purposes for power users, administrators, network administrators, or even normal users.

## Procedure

1.  To view the MITRE ATT&amp;CK Repository data, navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **MITRE ATT&amp;CK** &gt; **Tools**.

    You can view the listed tools.

2.  Click a tool to view all the associated information.

3.  Click **New** to manually create the MITRE ATT&amp;CK tools.

4.  Fill in the fields appropriately.

    |Field|Description|
    |-----|-----------|
    |ID|Unique ID for a course of action to prevent an attack.|
    |Revoked|Indicates that the revoked objects are no longer considered valid by the object creator.|
    |Name|Enter a descriptive name to identify the object.|
    |Source|Specifies the threat source from which this object record is created.|
    |Aliases|A list of other names to identify this object.|
    |Created Time In Source|Specifies the time the object is created in the source.|
    |Modified Time In Source|Specifies the time the object is modified in the source.|
    |Description|A description that provides more details and context about the object, potentially including its purpose and its key characteristics.|
    |Contributors|Specifies the contributors.|
    |**Insights**|
    |Notes|Any additional information related to the mitigation.|
    |**Additional Information**|
    |Additional Context|Add any additional context for this object.|
    |Comments|Add any comments for this object.|

5.  Click **Save**.

6.  To view how these objects are related, click **Relationships**.


**Parent Topic:**[MITRE-ATT&amp;CK Repository](../concept/tisc-mitre-att-ck-framework-overview.md)

