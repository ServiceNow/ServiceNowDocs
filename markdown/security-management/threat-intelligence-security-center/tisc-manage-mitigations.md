---
title: Manage Mitigations
description: Manage the mitigations that are imported from the MITRE TAXII collections. Mitigations enable you to prevent an adversary from successfully executing techniques or sub-techniques against your organization. In STIX, mitigations are known as course of actions.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MITRE-ATT&amp;CK Repository, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Manage Mitigations

Manage the mitigations that are imported from the MITRE TAXII collections. Mitigations enable you to prevent an adversary from successfully executing techniques or sub-techniques against your organization. In STIX, mitigations are known as course of actions.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  After you enable the MITRE ATT&amp;CK related feed data sources which are available in the base system, click **Execute Now** to run the integrations and fetch the MITRE related information.

    For more information on enabling the integrations.

2.  To view the MITRE ATT&amp;CK Repository data, navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **MITRE ATT&amp;CK** &gt; **Mitigations**.

    Click a mitigation to view all the associated information.

3.  Click **New** to manually create the MITRE ATT&amp;CK mitigations.

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


**Parent Topic:**[MITRE-ATT&amp;CK Repository](../concept/tisc-mitre-att-ck-framework-overview.md)

