---
title: Resolve conflicts
description: Resolve conflicts in ServiceNow Studio when applying remote or stashed changes that conflict with the local version of the same application file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-sc-resolving-conflicts.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Work with changes in Git, Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Resolve conflicts

Resolve conflicts in ServiceNow Studio when applying remote or stashed changes that conflict with the local version of the same application file.

## Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/link-app-to-source-control.md)

At least one stashed change must be applied.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Pull from a repository or apply stashed changes.

    If the system detects a conflict, the Resolve Conflicts modal appears and displays the conflicting files.

5.  Select an option to resolve the conflict.

    |Option|Description|
    |------|-----------|
    |**Select an action**|Apply or discard all stashed changes at once.|
    |**Manually merge changes**|Select individual changes to apply or discard.|

6.  To apply or discard all changes, select an **Action**.

    |Option|Description|
    |------|-----------|
    |**Take stashed changes**|Applies the application file version from the stashed changes.|
    |**Discard stashed changes**|Applies the application file version from the most recent pull from the repository.|

7.  Select **Apply Stashed Changes**.

8.  Select **Close dialog**.

9.  To merge conflicting changes individually, select **Manually Apply**.

    The ServiceNow AI Platform displays a list of the version differences by field.

10. Select the field values for the merged application file.

11. Select **Save Merge**.


## Result

The conflict is resolved and the application file reflects the selected changes. Continue with normal pull and push operations to update the Git repository.

**Parent Topic:**[Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-work-with-changes-in-git.md)

