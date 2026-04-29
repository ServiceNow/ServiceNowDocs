---
title: Manage Groups
description: Manage the groups that are imported from the MITRE TAXII collections. Groups are sets of related intrusion activity that are tracked by a common name in the security community. Analysts track clusters of activities using various terms such as threat groups, activity groups, threat actors, intrusion sets, and campaigns. In STIX, groups are known as intrusion sets.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MITRE-ATT&amp;CK Repository, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Manage Groups

Manage the groups that are imported from the MITRE TAXII collections. Groups are sets of related intrusion activity that are tracked by a common name in the security community. Analysts track clusters of activities using various terms such as threat groups, activity groups, threat actors, intrusion sets, and campaigns. In STIX, groups are known as intrusion sets.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  To view the MITRE ATT&amp;CK Repository data, navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **MITRE ATT&amp;CK** &gt; **Groups**.

    You can view the listed groups.

2.  Click **New** to manually create the MITRE ATT&amp;CK groups.

3.  Fill in the fields appropriately.

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
    |**Insights**|
    |Notes|Any additional information related to the mitigation.|
    |**Additional Information**|
    |Additional Context|Add any additional context for this object.|
    |Comments|Add any comments for this object.|

4.  Click **Save**.

5.  To view how these objects are related, click **Relationships**.


**Parent Topic:**[MITRE-ATT&amp;CK Repository](../concept/tisc-mitre-att-ck-framework-overview.md)

