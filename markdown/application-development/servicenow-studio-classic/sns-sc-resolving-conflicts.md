---
title: Resolve conflicts
description: Resolve conflicts in ServiceNow Studio before applying remote or stashed changes. Conflicts occur when there are multiple change versions of the same application file: one set of changes in the remote or stashed version and another set of changes in the local version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sns-sc-resolving-conflicts.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work with changes in Git, Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Resolve conflicts

Resolve conflicts in ServiceNow Studio before applying remote or stashed changes. Conflicts occur when there are multiple change versions of the same application file: one set of changes in the remote or stashed version and another set of changes in the local version.

## Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/link-app-to-source-control.md)

You must have one or more stashed changes applied.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Pull from a repository or stash local changes.

    If the system detects a conflict, the Resolve Conflicts modal appears.

5.  Select an option to resolve the conflict.

    |Option|Description|
    |------|-----------|
    |**Select an action**|Option to apply or discard all stashed changes.|
    |**Manually merge changes**|Option to individually select which changes to apply.|

6.  If you want to apply or discard all changes, select an **Action**.

    |Option|Description|
    |------|-----------|
    |**Take stashed changes**|Applies the application file version from the stashed changes.|
    |**Discard stashed changes**|Applies the application file version from the most recent pull from the repository.|

7.  Select **Apply Stashed Changes**.

8.  Select **Close dialog**.

9.  If you want to merge the conflicting changes, select **Manually Apply**.

    The ServiceNow AI Platform displays a list of the version differences by field.

10. Select the field values you want the merged application file to have.

11. Select **Save Merge**.


**Parent Topic:**[Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-sc-work-with-changes-in-git.md)

