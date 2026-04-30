---
title: Example - Create a group for all Biomed location support managers
description: Explore how a group can be created that contains the correct roles location support managers which users can then be added to in order to inherit those permissions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-10"
reading_time_minutes: 1
breadcrumb: [Create a group for all location managers, Configure, Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Example - Create a group for all Biomed location support managers

Explore how a group can be created that contains the correct roles location support managers which users can then be added to in order to inherit those permissions.

## Before you begin

Role required: admin

## About this task

Armand is a ServiceNow administrator for a hospital who needs to set up Alectri Health Santa Clara Biomed support managers as users. Armand decides to create a group for all support managers in ServiceNow that includes the sn\_cto\_biomed.loc\_support\_manager role. Users added to that group will then inherit the correct biomed support manager permissions.

## Procedure

1.  Navigate to **All &gt; User Administration &gt; Groups**.

2.  Select **New**.

3.  In the name field, enter **Biomed Alectri Santa Clara Location Support Manager.**.

4.  In the Description field, enter **Any user who will be a Biomed support manager for the Alectri Santa Clara Biomed support department**.

5.  Fill in other fields as needed.

6.  Navigate to the roles related list.

7.  Click **Edit**.

8.  Add the **sn\_cto\_biomed.loc\_support\_manager** role into the Roles List.

9.  Click **Save**.


## Result

A group for all biomed location support managers has been created. Armand can assign biomed support mangers users to this group as needed.

