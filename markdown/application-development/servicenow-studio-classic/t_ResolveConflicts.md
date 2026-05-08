---
title: Legacy - Resolve conflicts
description: Application developers can choose which application file version to use when applying remote or stashed changes.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Resolve conflicts

Application developers can choose which application file version to use when applying remote or stashed changes.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   Role required: admin
-   Link an application to source control
-   Apply a stashed change

## About this task

Conflicts occur when there are multiple change versions of the same application file: one set of changes in the remote or stashed version and another set of changes in the local version. Studio requires developers resolve conflicts before applying remote or stashed changes.

## Procedure

1.  From Studio, apply remote or stash changes.

    If the system identifies a conflict, it displays the Resolve Conflicts dialog.

2.  Select how to resolve the conflict.

<table id="choicetable_pqx_jdv_lv"><tbody><tr><td id="d65401e140">

**Select an action**

</td><td>

Apply or discard all stashed changes. Go to [Step 3](t_ResolveConflicts.md#SelectAction).

</td></tr><tr><td id="d65401e153">

**Manually merge changes**

</td><td>

Individually select which changes to apply. Go to [Step 6](t_ResolveConflicts.md#Merge).

</td></tr></tbody>
</table>3.  If you want to apply or discard all stashed changes, select an **Action**.

<table id="choicetable_wln_1bv_lv"><tbody><tr><td id="d65401e178">

**Take Stashed Changes**

</td><td>

Applies the application file version from the stashed changes.

</td></tr><tr><td id="d65401e187">

**Discard Stashed Changes**

</td><td>

Applies the application file version from the most recent pull from the repository.

</td></tr></tbody>
</table>4.  Click **Apply Stashed Changes**.

    The system applies the selected changes.

5.  Click **Close Dialog**.

6.  If you want to merge the conflicting changes, click **Manually Apply**.

    The system displays a list of version differences by field.

7.  Select the field values you want the merged application file to have.

8.  Click **Save Merge**.

    The system applies the selected changes.


**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

