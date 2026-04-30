---
title: Manage Matrices
description: Manage the matrices that are imported from the MITRE TAXII collections. Matrices are a collection of tactics and techniques. You can view the matrices to review if your collections are available in the MITRE-ATT&amp;CK repository.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [MITRE-ATT&amp;CK Repository, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Manage Matrices

Manage the matrices that are imported from the MITRE TAXII collections. Matrices are a collection of tactics and techniques. You can view the matrices to review if your collections are available in the MITRE-ATT&amp;CK repository.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  After you enable the MITRE ATT&amp;CK related feed data sources which are available in the base system, click **Execute Now** to run the integrations and fetch the MITRE related information.

    For more information on enabling the integrations

2.  To view the MITRE ATT&amp;CK Repository data, navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **MITRE ATT&amp;CK**.

    The MITRE ATT&amp;CK related records are displayed. By default all the records are in enabled state.

    **Note:** You can enable only those matrices that are relevant to your organization.

3.  Select any Matrix record and click **Disable** if you want to disable any specific record.

4.  Alternatively, you can create new matrices record by clicking **New** to manually to create the MITRE ATT&amp;CK matrices.

5.  Fill in the fields appropriately.

    |Field|Description|
    |-----|-----------|
    |Name|Enter the name of the matrix.|
    |Source|Specifies the threat source from which this record is created.|
    |Active|Select this check box to active the matrix record.|
    |Created Time In Source|Specifies the time the object is created in the source.|
    |Modified Time In Source|Specifies the time the object is modified in the source.|
    |Description|A description that provides more details and context about the intrusion set, potentially including its purpose and its key characteristics.|
    |**Insights**|
    |Notes|Any additional information related to the mitigation.|
    |**Additional Information**|
    |Additional Context|Add any additional context for this object type.|
    |Comments|Add any comments that you might have in addition.|


**Parent Topic:**[MITRE-ATT&amp;CK Repository](../concept/tisc-mitre-att-ck-framework-overview.md)

