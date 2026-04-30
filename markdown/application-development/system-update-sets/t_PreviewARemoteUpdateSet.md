---
title: Preview a remote update set
description: Previewing compares an update set retrieved from a remote instance to updates on the local instance to detect potential problems. You must preview an update set and address all problems before you can commit the update set.The process of previewing an update set creates a preview record for each update. You can review the preview records to make sure that the correct updates are being committed.Preview an update set to detect and resolve problems that may occur if you commit the updates on the local instance.
locale: en-US
release: xanadu
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Update set transfers, System update sets, Deploying applications, Building applications]
---

# Preview a remote update set

Previewing compares an update set retrieved from a remote instance to updates on the local instance to detect potential problems. You must preview an update set and address all problems before you can commit the update set.

## Procedure

1.  If the system property **glide.update\_set.auto\_preview** is set to **true**, the system automatically starts the preview process after the update set is retrieved.

    If this property is **false**, the preview process must be started manually.

    1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  Click **Preview Update Set**.

    For large update sets, the preview process may require a significant amount of time. If necessary, you can cancel the preview process by clicking the **Cancel** button on the progress dialog box.

    The Update Set Preview page shows results and lists problems. Read the information and click **Close**.

2.  On the Retrieved Update Set form, make a selection.

    |Option|Action|
    |------|------|
    |**If no problems were detected**|Click **Commit Update Set** to commit all changes on the instance without reviewing the preview results.|
    |**If problems were detected**|Address each problem in the Update Set Preview Problems related list.|

    ![Retrieved update set form](../image/RetrievedUpdateSetForm.png "Retrieved Update Set form")

3.  Preview the records.

    1.  Open the update set record and click **Show All Preview Records** to make sure the correct updates are being committed.

    2.  Open the update set record and click **Run Preview Again** to run the comparisons again.

    3.  Review the **Update Set Preview Problems** related list to ensure that the correct updates are being committed.


**Parent Topic:**[Update set transfers](../reference/update-set-transfers.md)

## Review a preview record for an update set

The process of previewing an update set creates a preview record for each update. You can review the preview records to make sure that the correct updates are being committed.

### Procedure

1.  Open the Update Set record and preview the update set.

2.  Click the **Show All Preview Records** related link.

3.  Click the **Disposition** to open a preview record and then review the information \(see table\).

4.  Fill in the fields on the form, as appropriate.

    ![Update set preview](../image/PreviewRecordForm.png "Update set preview")

<table id="table_b4g_gzw_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disposition

</td><td>

Indicates when a collision is detected:-   **Collision/Update**, **Collision/Insert**, or **Collision/Delete:** the change is older than a change to the same object on the local instance.
-   **Update**, **Insert**, or **Delete:** the change does not conflict with a change on the local instance.


</td></tr><tr><td>

File differences

</td><td>

Compares the most recent version of the object on the local instance with the version in the update set. Differences are marked with a color key. Deletions are highlighted in red, additions in green, and modifications in yellow.

</td></tr><tr><td>

Proposed action

</td><td>

Indicates how to handle the change when the update set is committed.-   **Commit:** Accept the change in the remote update. The default proposed action for every preview record is Commit, even if a newer update exists on the instance.
-   **Skip:** Reject the change.


</td></tr></tbody>
</table>5.  If necessary, resolve any problems listed in the **Update Problems** related list.

6.  In the Proposed action field, select the action to take when committing the update set.

7.  Click **Update** to save the action.

8.  Repeat the process for every preview record.


## Resolve a preview problem in an update set

Preview an update set to detect and resolve problems that may occur if you commit the updates on the local instance.

### Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

2.  Open the update set record and scroll to the **Update Set Preview Problems** related list.

    ![Update set preview problems](../image/UpdateSetsCollisionList.png "Upset Set Preview Problems")

3.  Review each problem description to determine the cause and resolve the problem.

    Update Set Preview Problems

    -   **Missing Object**

        Example problem text: `Could not find a record in sys_ui_policy referenced in this update`.

        Description: The object or a referenced object does not exist on the target instance. For example:

        -   An update modifies the form layout for a table that has not been created in the local instance.
        -   A UI policy action is included in the update set, but the parent UI policy is not.
        -   Resolution: Create another update set on the source instance to transfer the missing object to the local instance, or create the object on the local instance. Use these **Available Actions** to assist in problem resolution:
            -   **Find missing field** or **Find missing record**: Opens a new window and searches the source instance for the missing field \(dictionary entry\) or record.
            -   **Find missing update**: Opens a new window and searches the source instance for the update record that corresponds to the missing field or record.
    -   **Collision**

        Example problem text: `Found a local update that is newer than this one`

        Description: A change in the update set is older than a change to the same object on the local instance.

        Resolution: Compare the two updates and determine which version to use. To use the version on the local instance, select **Skip remote update**. To use the version in the update set, select **Accept remote update**. Use these **Available Actions** to assist in problem resolution:

        -   **Compare with local**: opens the preview record, which provides a comparison of the differences between the local version and the version in the update set.
        -   **Show local field** or **Show local record**
        -   **Show local update**
    -   **Uncommitted update**

        Example problem text: `Could not find a table field (u_case.u_reference) referenced in this update, but did find it in another uncommitted update set`

        Description: The object exists in another remote update set that has not been committed.

        Resolution: Commit the other remote update set first or move this update to the other update set. Use these **Available Actions** to assist in problem resolution:

        -   **Show uncommitted update**: opens the update record in the other remote update set.
        -   **Show uncommitted Update Set**: open the other remote update set record.
    -   **Table to be deleted has data**

        Example problem text: `Found a row in the table that is going to be deleted`

        Description: One difference between table deletes and other metadata deletes is that the table data is lost when the table is deleted. \(If the table is empty \(no rows\), then no problem is generated.\)

        Resolution: The problem must be ignored \(delete will happen\) or skipped \(delete will not happen\) before the update set can be committed. You can restore the table, but the restore does not bring back the data.

        You are not allowed to delete system tables \(ServiceNow tables\) or tables outside your application scope.

    -   **Application scope validation issue**

        Description: The previewer identifies the following combination of states as a problem:

        -   The scope for the update set is not Global and
        -   The application is not found on the target instance and
        -   The application is not included with the update set and
        -   The application is not found on the ServiceNow Store.
        Resolution: Transfer the update set only to instances that include the application scope or ensure that the update set includes the application.

    -   **Conflict within a single batch**

        Example problem text: `This update has conflicts within the update set with the same name. Resolve the issue on the source system and re-preview or choose a specific update to use.`

        Description: Two or more update sets within the same batch have conflicting changes. The **Update Set Preview Problems**list contains a record for each update set with a conflicting change.

        Resolution: Compare the conflicting update sets and determine which version to use. If you know which update set is the correct one to use, select the row for that set and click **Accept this collision.** Otherwise, click **Compare Collisions** to compare the conflicting update sets.

        ![Compare two Updates form](../image/UpdateSetCompare.png "Compare two Updates")

        From this screen, you can compare any two of the conflicting update sets and choose the update set to commit.


