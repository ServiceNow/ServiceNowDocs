---
title: Publish a custom workflow activity
description: When a user creates a custom activity and saves or submits it, that activity appears in the Custom and Packs tabs of the designer palette, but is only visible to the user who created it.
locale: en-US
release: xanadu
product: Workflow Activities
classification: workflow-activities
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow activities, Classic Workflow, Build workflows]
---

# Publish a custom workflow activity

When a user creates a custom activity and saves or submits it, that activity appears in the **Custom** and **Packs** tabs of the designer palette, but is only visible to the user who created it.

When configuration is complete, the user clicks **Publish**, which makes the activity accessible to other users on the instance with the workflow\_admin or activity\_creator role. Published activities are available for upload to the ServiceNow Store, can be added to workflows, and can be edited by any user with the proper roles.

To edit a published activity, click **Checkout**. When an activity is checked out by a user, only that user can modify it. The fields of a checked out activity are read-only for all other users. When the checked out activity has been modified successfully, the user publishes it again. The system adds a new version of this activity to the Custom tab in the Workflow Editor palette.

**Note:** Activities you create and publish are only visible in the Packs tab if they were created in the current application scope.

## Locked versions

Problems can arise if an activity version is checked out by a user and not checked back in, for example, when the user is sick or leaves the company. An activity in this state cannot be checked out for update.

A user with the admin role can return a locked activity to a published state. The administrator opens the locked activity from the **Custom** tab of the Workflow Editor, selects the checked-out version, and selects **Force Checkout**, and then **Publish**.

