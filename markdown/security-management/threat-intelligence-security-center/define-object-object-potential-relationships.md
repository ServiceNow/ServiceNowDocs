---
title: Confirm object-object potential relationships
description: Define the potential relationships between the objects.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Potential Relationships, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Confirm object-object potential relationships

Define the potential relationships between the objects.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Potential Relationships** &gt; **Object-Object**.

4.  Select the observable record.

5.  Click **Confirm Relation**.

    A Potential relationship record is ideally created which is identified based on its correlation rules. Once you confirm the relationship from this section, then the observables record will move to the Relationships section which means that the relation between the observables to observables is confirmed. The record shows a confirmed relation only when the correlation rules are matched. For example, a potential relationship can be created when two observables of type URLs has the same domain name.

    Alternatively, you can also create new observables record by linking the observables from the list of observables and confirm the relationships from the related records tab of each observable.

    1.  Open any Observable record.

    2.  Go to **Related Records** tab.

    3.  Click the **Link** button.

    4.  Select one or more observable\(s\).

    5.  Click **Link**.

        This will create a new relationship between the selected observable record and the newly linked observables.

6.  Click **Delete** to delete the relationships.


**Parent Topic:**[Potential Relationships](../concept/potential-relationships.md)

