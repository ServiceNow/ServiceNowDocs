---
title: Setting up roles and responsibilities for Healthcare Operations users
description: To manage access effectively in Healthcare Operations Core \(HCO\), first understand how roles and responsibilities work together. These concepts build on the Service Model Foundation \(SMF\) but are adapted for HCO-specific use cases.
locale: en-US
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Setting up roles and responsibilities for Healthcare Operations users

To manage access effectively in Healthcare Operations Core \(HCO\), first understand how roles and responsibilities work together. These concepts build on the Service Model Foundation \(SMF\) but are adapted for HCO-specific use cases.

## Roles

Roles define table-level access. They determine which objects you can interact with and what actions you can perform. IE, \(CRUD: Create, Read, Update, Delete\).

Example: The `sn_hco.care_team_member` role enables you to work with HCO cases.

## Responsibilities

Responsibilities control record-level access within tables. Even if your role grants access to a table, responsibilities decide which specific records you can view or edit.

Responsibilities in HCO are based on Service Model Foundation responsibilities, but adapted \(relabeled\) for healthcare operations using Related Party Configurations.

Example: The Care Team Member responsibility limits your access to cases for healthcare organizations that you’re a member of.

|Healthcare Operations Core Responsibility|Inherited Service Model Foundation responsibility|
|-----------------------------------------|-------------------------------------------------|
|Care Team Member|Service location business contributor|
|Care Team Manager|Service location business manager|
|Support Department Agent|Location Support Agent|

## Why responsibilities matter

Think of roles as the door to the building and responsibilities as the rooms you’re allowed to enter.

This layered approach segregates data so that members of healthcare organizations only see records that pertain to that healthcare organization that they have responsibility for.

## Example scenario

You’re a care team member associated with the Intensive Care Unit \(ICU\) at a hospital.

-   Role: The `sn_hco.care_team_member` role gives you access to HCO cases.
-   Responsibility: The Care Team Member responsibility restricts access to cases within that ICU only.

Result: You can work on HCO cases related to that ICU, but can’t view cases for other units.

|Role|Responsibility|Description|
|----|--------------|-----------|
|`sn_hco.care_team_member`|Care Team Member|Use the Care Team Member responsibility to work on cases to report issues within an assigned unit.|
|`sn_hco.care_team_manager`|Care Team Manager|Use the Care Team Manager responsibility to report issues within an assigned unit and manage the members of your healthcare organization.|
|`sn_hco.loc_support_agent`|Support Department Agent|The Support Department Agent responsibility is used by the Care Team Operations applications so agents can fulfill cases for their specific department.|

## What to do next

-   [Assign roles to Healthcare Operations Core users](../task/assign-roles-cto-users.md)
-   [Assign responsibilities to Healthcare Operations Core users](../task/hco-assign-responsibilities.md)

