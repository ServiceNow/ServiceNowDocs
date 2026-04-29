---
title: Working with update sets
description: Manage your customizations and resolve potential collisions before you move them to another instance.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [System update sets, Deploying applications, Building applications]
---

# Working with update sets

Manage your customizations and resolve potential collisions before you move them to another instance.

To create an update set see [Create and select an update set as the current set](../task/create-select-update-set.md).

When the update set is completed, you can transfer the update set to another instance according to your test process. See [Update set transfers](../reference/update-set-transfers.md).

If a customization is made in the wrong update set

1.  Switch to the desired update set.
2.  Modify the object \(record\) that was originally changed. You can make a trivial change, such as adding a field.
3.  Save the record.
4.  Back out the change just performed, and then save the record again.

    This action ensures that the latest version of the object is included in the desired update set and prevents duplicate updates for the same object in a single update set.


Don't change the **Update Set** field value in a Customer Update record.

-   **[Create and select an update set as the current set](../task/create-select-update-set.md)**  
Create an update set to store customization changes and select it as the current set.
-   **[Select the current update set in Unified Navigation](../task/select-update-set-system-settings.md)**  
You can change the current update set at any time using the update set picker in Unified Navigation.
-   **[View customizations and compare with current version](../task/view-customer-update-records.md)**  
View the customizations that make up an update set and compare the update to the current version.
-   **[Navigation between records](../task/navigation-between-records.md)**  
Navigate between a customer update record and the customized object or the application file for the object.
-   **[Compare local update sets](../task/t_CompareLocalUpdateSets.md)**  
Administrators can preview local and remote \(retrieved\) update sets and compare the sets with one another to resolve conflicting changes.
-   **[Preview a remote update set](../task/t_PreviewARemoteUpdateSet.md#)**  
Previewing checks a retrieved update set against the local instance to find issues. Resolve all problems before committing the update set.
-   **[Commit an update set](../task/t_CommitAnUpdateSet.md)**  
After resolving any issues from previewing, commit the update set to apply all changes and generate a local copy with records of each update.
-   **[Retrieve an update set](../task/t_RetrieveAnUpdateSet.md)**  
Retrieve completed update sets from another instance.
-   **[Back out an update set](../task/t_BackOutUpdateSet.md)**  
You can back out changes to existing records for any committed update set.
-   **[Mark an update set complete](../task/t_CompleteUpdateSets.md)**  
When you have completed the customizations and compared local update sets to resolve conflicts, mark the update set as Complete.

**Parent Topic:**[System update sets](system-update-sets.md)

