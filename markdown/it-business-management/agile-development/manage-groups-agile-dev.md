---
title: Assignment groups in Agile Development 2.0
description: Learn the requirements to create and manage your assignment groups in Agile Development 2.0.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Agile Development 2.0, Strategic Portfolio Management]
---

# Assignment groups in Agile Development 2.0

Learn the requirements to create and manage your assignment groups in Agile Development 2.0.

## Creating assignment groups

Creating assignment groups in Agile Development 2.0 

A user with the admin role can create assignment groups of the type **Agile Team**. Your scrum teams are represented by these agile groups, which you can use to assign to work items such as stories and epics. For more information, see [Create an assignment group in Agile Development 2.0](../task/create-an-agile-group.md#).

## Adding members to assignment groups

-   New customers: After an agile group is created, you can request your admin to [add](../task/add-group-members-to-group.md) members to the group.
-   Existing customers: If you upgraded to the Xanadu release, a user with the scrum\_admin role or the scrum\_master role can add members to your agile group.

    **Note:** You can restrict this function just to the admin by creating the **scrum.disallow\_scrum\_add\_group\_member** property and setting it to **true**. For information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).


For information on the procedure to add members to groups, see [Add members to an assignment group in Agile Development 2.0](../task/add-group-members-to-group.md)

## Capacity of an assignment group

For each group member, a default number of story points can be defined. At the group level, the sum of these story points determines the group capacity.

-   **[Create an assignment group in Agile Development 2.0](../task/create-an-agile-group.md#)**  
Create an assignment group of the type Agile Team so that you can assign these groups to a product or a release.
-   **[Convert a release team to a group \(only for existing customers having release teams\)](../task/convert-release-team-to-group.md)**  
Convert an existing release team to an assignment group of type Agile Team so that you can assign them to a product or a release.
-   **[Add members to an assignment group in Agile Development 2.0](../task/add-group-members-to-group.md)**  
Add members who would work on the scrum stories and tasks.

**Parent Topic:**[Using Agile Development 2.0](using-agile-development-2-0.md)

