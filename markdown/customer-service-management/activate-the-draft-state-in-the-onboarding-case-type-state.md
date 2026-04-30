---
title: Activate the draft state in the onboarding case type state
description: A portal user can save a case during the intake process and continue later​ with the draft state.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up predefined Playbooks for Portals, Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Activate the draft state in the onboarding case type state

A portal user can save a case during the intake process and continue later​ with the draft state.

## About this task

Activate a draft state for the onboarding case type so that the case remains in the draft state during the intake stage until the case is submitted.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_choice.list**.

2.  Select the record with **Table name** - **sn\_onboarding\_case** with the **Element** field value as **state**, and the **Label** field name as **Draft**.

3.  Select **Edit**.

4.  Clear the **Inactive** check box.

5.  Select **Update**.

6.  Navigate to **System Definition** &gt; **Scheduled Job** and search for **sys\_id** - **ba5ba3d8944e7110f87759453e4c7084** or **Name** - **Update My Lists URL for draft cases**.

7.  Select **Execute Now**.

    This action excludes the Draft cases from the list filter on the **My List** tab on the initial page load.

8.  If you’re using a custom case type table and you do not see the relevant state upon filtering, you might have to assign requisite ACLs for the state field and its associated values.


