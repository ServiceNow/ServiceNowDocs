---
title: Set up element variable for BIA dependency assessment grid
description: As a functional system administrator, you can set up an element variable that is specific custom columns, which are required for a particular dependency of an element.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Grid configuration, BCM in the Classic Workspace, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up element variable for BIA dependency assessment grid

As a functional system administrator, you can set up an element variable that is specific custom columns, which are required for a particular dependency of an element.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **General Administration** &gt; **Element Variables**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Model|Element definition \[sn\_bcm\_element\_definition\] reference. You can create multiple element variables for an element definition.|
    |Type|Field class in the model table.|
    |Label|Display name in the dependency group of the BIA dependency grid.|
    |Column name|Name of the column in the table.|
    |Active|Option to activate the element variable.|
    |Read only|Option to render the element variable as read only.|
    |Mandatory|Option to set the element variable as mandatory.|
    |Display|Option to display the element variable.|
    |Enable reporting|Option to report the element variable.|
    |Reference Specification|
    |Reference|Reference to the table that has the element variable.|
    |Reference qual condition|Filter conditions set for the reference.|
    |Choice List Specification|
    |Choice|Specification of list choice.|
    |Default Value|
    |Default value|Description for the default value.|

4.  Click **Submit**.


