---
title: Add incidents by same caller related list
description: This example adds the existing relationship, Incidents by Same Caller, to incident forms.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create defined related lists, Related lists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Add incidents by same caller related list

This example adds the existing relationship, Incidents by Same Caller, to incident forms.

## Before you begin

Role required: admin

## About this task

-   **Applies to table**: This list appears as an available related list when viewing an incident record.
-   **Queries from table**: This list displays a list of incidents.
-   **Query with**: This script selects records where the **caller\_id** matches the **caller\_id** of the parent record \(the incident you are viewing\).

![Relationship record.](../image/Relationship.png)

## Procedure

1.  Open an incident.

2.  Right-click the header and select **Configure** &gt; **Related Lists**.

    The name of the existing relationships appears in your list of available lists.

3.  Move the **Incidents by Same Caller** list to the **Selected** list.

4.  Click **Save**.

    ![Incident with the related list of other incidents for the caller.](../image/Relationship3.png)


## What to do next

Notes and limitations:

-   Creating a record using a related list applies the list filter to the record and auto-populates the related field. This behavior applies to reference, string, Boolean, and menu fields when the criteria in the filter is set to **is** or **=**.
-   For example, if you click the **New** button on one of these new relationships, the system attempts to ensure that the new record matches the list conditions. For example, clicking **New** on the example list results in an incident where the **caller\_id** is pre-populated with **Bud Richman**.
-   When scripting your condition, **current** is the record to which you want to add queries while **parent** is the main record being displayed.
-   These relationships do not refresh until you update a form. In the example, if you changed the caller from **Bud Richman** to **Fred Luddy**, the list at the bottom of the screen still displays the incidents belonging to Bud Richman until you save the incident.
-   You are not limited to a single query condition. It is, for example, possible to have a related list of all incidents opened by the same caller in the last week, or all **open** incidents opened by the same caller.
-   The **current** and **parent** objects cannot be used with the **Queries from** field. Instead, the **gs** object is available for GlideSystem calls.
-   The **Edit** button is not available on defined relationships, as the relationship is scripted.

Additional use case: You can enable a similar relationship for the Request table to display **Requests by the Same Caller** using **Requested For** on the Request table.

**Parent Topic:**[Create defined related lists](t_CreateDefinedRelatedLists.md)

**Related topics**  


[GlideSystem](https://www.servicenow.com/docs/access?context=p_GlideServerAPIs&version=xanadu&pubname=xanadu-application-development&section=c_GlideSystem&ft:locale=en-US)

