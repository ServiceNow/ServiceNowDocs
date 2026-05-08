---
title: Resolve conflicts
description: App developers can select the app file version to use when applying remote or stashed changes in App Engine Studio \(AES\).
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use AES with a Git source control repository, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Resolve conflicts

App developers can select the app file version to use when applying remote or stashed changes in App Engine Studio \(AES\).

## Before you begin

-   Role required: admin
-   Link an application to source control
-   Apply a stashed change

## About this task

Conflicts occur when there are multiple change versions of the same application file: one set of changes in the remote or stashed version and another set of changes in the local version. App Engine Studio requires developers to resolve conflicts before applying remote or stashed changes.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Pull from a repository or stash local changes.

    If the system identifies a conflict, it displays the Resolve Conflicts dialog.

4.  Select how to resolve the conflict.

<table id="choicetable_pqx_jdv_lv"><tbody><tr><td id="d215900e106">

**Select an action**

</td><td>

Apply or discard all stashed changes. Go to step 3.

</td></tr><tr><td id="d215900e115">

**Manually merge changes**

</td><td>

Individually select which changes to apply. Go to step 6.

</td></tr></tbody>
</table>5.  If you want to apply or discard all stashed changes, select an **Action**.

<table id="choicetable_wln_1bv_lv"><tbody><tr><td id="d215900e136">

**Take Stashed Changes**

</td><td>

Applies the application file version from the stashed changes.

</td></tr><tr><td id="d215900e145">

**Discard Stashed Changes**

</td><td>

Applies the application file version from the most recent pull from the repository.

</td></tr></tbody>
</table>6.  Select **Apply Stashed Changes**.

    The system applies the selected changes.

7.  Select **Close Dialog**.

8.  If you want to merge the conflicting changes, select **Manually Apply**.

    The system displays a list of version differences by field.

9.  Select the field values you want the merged application file to have.

10. Select **Save Merge**.

    The system applies the selected changes.


**Parent Topic:**[Use AES with a Git source control repository](../concept/aes-source-control-use.md)

