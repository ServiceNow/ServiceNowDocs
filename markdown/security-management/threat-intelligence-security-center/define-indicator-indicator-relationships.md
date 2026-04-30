---
title: Define indicator-indicator relationships
description: Define relationships between the indicator object and other Use the relationships objects to link together two observables or an observable and SDO to explain how they relate to each other..
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Relationships Objects, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define indicator-indicator relationships

Define relationships between the indicator object and other Use the relationships objects to link together two observables or an observable and SDO to explain how they relate to each other..

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Relationships** &gt; **Indicator-Indicator**.

4.  Click **New**.

5.  Complete the fields in the form as appropriate.

<table id="choicetable_uvs_2cc_nzb"><thead><tr><th align="left" id="d312047e102">

Field

</th><th align="left" id="d312047e105">

Description

</th></tr></thead><tbody><tr><td id="d312047e111">

**Description**

</td><td>

Specifies the threat source from which this record is created.

</td></tr><tr><td id="d312047e120">

**Domain**

</td><td>

Defines the scope of the object record. The value in this field is auto populated.

</td></tr><tr><td id="d312047e131">

**Target Indicator**

</td><td>

Select and define the target indicator object.

</td></tr><tr><td id="d312047e140">

**Relationship Type**

</td><td>

A description that provides more details and context about the relationship type. Define the relationship direction whether it is direct or inverse.

-   Inverse - This is the type of relationship between the observable and object.
-   Direct - This is the type of relationship between the object and observable.


</td></tr><tr><td id="d312047e160">

**Source Indicator**

</td><td>

Select and define the source object indicator.

</td></tr></tbody>
</table>6.  Click **Submit**.


**Parent Topic:**[Relationships Objects](../concept/relationship-objects.md)

