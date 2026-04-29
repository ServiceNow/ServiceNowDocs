---
title: Preview a remote update set
description: Previewing checks a retrieved update set against the local instance to find issues. Resolve all problems before committing the update set.The process of previewing an update set creates a preview record for each update. You can review the preview records to make sure that the correct updates are being committed.Preview an update set to detect and resolve problems that may occur if you commit the updates on the local instance.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Working with update sets, System update sets, Deploying applications, Building applications]
---

# Preview a remote update set

Previewing checks a retrieved update set against the local instance to find issues. Resolve all problems before committing the update set.

## Before you begin

Role required: admin

If the system property glide.update\_set.auto\_preview is set to `true`, the system automatically starts the preview process after the update set is retrieved. If this property is `false`, the preview process must be started manually.

## Procedure

1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**

2.  Select **Preview Update Set**.

    For large update sets, the preview process may require a significant amount of time. If necessary, you can cancel the preview process by selecting the **Cancel** button on the progress dialog box.

    The Update Set Preview page shows results and lists problems. Read the information and select **Close**.

3.  Preview the records.

    1.  Open the update set record and select **Show All Preview Records** to make sure that the correct updates are being committed.

    2.  Open the update set record and select **Run Preview Again** to run the comparisons again.

    3.  Review the **Update Set Preview Problems** related list to verify that the correct updates are being committed.

4.  On the Retrieved Update Set form, select **Commit Update Set** to commit all changes on the instance without reviewing the preview results.

    If problems were detected, address each problem in the Update Set Preview Problems related list.


**Parent Topic:**[Working with update sets](../concept/using-system-update-sets.md)

## Review a preview record for an update set

The process of previewing an update set creates a preview record for each update. You can review the preview records to make sure that the correct updates are being committed.

### Before you begin

Role required: admin

### Procedure

1.  Open the Update Set record and preview the update set.

2.  Select the **Show All Preview Records** related link.

3.  Select the **Disposition** to open a preview record.

4.  Fill in the form.

<table id="table_b4g_gzw_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disposition

</td><td>

Indicates when a collision is detected. If the change predates a local modification to the same object. -   Collision
-   Update
-   Insert
-   Delete


</td></tr><tr><td>

File differences

</td><td>

Compares the latest local object version with the update set, marking differences with colors.

-   Additions are marked green.
-   Changes are marked yellow.
-   Deletions are marked red.


</td></tr><tr><td>

Proposed action

</td><td>

Specifies the procedure for managing the change once the update set has been committed. -   **Commit**

Accept the change in the remote update. The default proposed action for every preview record is to commit, even if a newer update exists on the instance.

-   **Skip**

Reject the change.

</td></tr></tbody>
</table>5.  Resolve any problems listed in the **Update Problems** related list.

6.  In the proposed action field, select the action to take when committing the update set.

7.  Select **Update** to save the action.


## Resolve a preview problem in an update set

Preview an update set to detect and resolve problems that may occur if you commit the updates on the local instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

2.  Open the update set record and scroll to the **Update Set Preview Problems** related list.

3.  Review each problem description to determine the cause and resolve the problem.

<table id="table_vqn_m1v_1hc"><thead><tr><th>

Problem

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Missing Object

</td><td>

The object or a referenced object doesn’t exist on the target instance. Create another update set on the source instance to transfer the missing object to the local instance, or create the object on the local instance.-   Open a new window with the **Find missing field** or **Find missing record** and search the source instance for the missing field or record.
-   Open a new window with **Find missing update** and search the source instance for the update record that corresponds to the missing field or record.


</td></tr><tr><td>

Collision

</td><td>

A change in the update set is older than a change to the same object on the local instance. Compare the two updates and determine which version to use.-   To use the version on the local instance, select **Skip remote update**.
-   To use the version in the update set, select **Accept remote update**
-   To use the version in the update set, select Accept remote update.
-   Open the preview record with **Compare with local** to view a comparison of the differences between the local version and the version in the update set.
-   Show local field
-   Show local record
-   Show local update


</td></tr><tr><td>

Uncommitted update

</td><td>

The object exists in another remote update set that hasn’t been committed. Commit the other remote update set first or move this update to the other update set. -   **Show uncommitted update** opens the update record in the other remote update set.
-   **Show uncommitted Update Set** opens the other remote update set record.


</td></tr><tr><td>

Table to be deleted has data

</td><td>

Deleting a table removes its data, unlike other metadata deletions. Skip or ignore related issues before committing updates. Restoring the table doesn’t recover its data.

**Note:** You can't delete system tables or tables outside of your application scope.

</td></tr><tr><td>

Application scope validation issue

</td><td>

The previewer identifies the following combination of states as a problem:-   The scope for the update set isn’t Global.
-   The application isn’t found on the target instance.
-   The application isn’t included with the update set.
-   The application isn’t found on the ServiceNow Store.
Transfer the update set only to instances that include the application scope or confirm that the update set includes the application.

</td></tr><tr><td>

Conflict within a single batch

</td><td>

Two or more update sets within the same batch have conflicting changes. The **Update Set Preview Problems** list contains a record for each update set with a conflicting change.-   Compare the conflicting update sets and determine which version to use.
-   Select **Compare Collisions** to compare the conflicting update sets.
-   Select **Accept this collision**.


</td></tr></tbody>
</table>
