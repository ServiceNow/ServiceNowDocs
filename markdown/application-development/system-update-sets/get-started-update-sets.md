---
title: Get started with update sets
description: Because update sets make changes to an instance, review this information to avoid errors and performance issues. Learn how to plan the update process and avoid common mistakes.
locale: en-US
release: yokohama
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [System update sets, Deploying applications, Building applications]
---

# Get started with update sets

Because update sets make changes to an instance, review this information to avoid errors and performance issues. Learn how to plan the update process and avoid common mistakes.

## When to use update sets

<table id="deploymentOptionTable"><thead><tr><th>

Deployment option

</th><th>

Good for

</th><th>

Future considerations

</th></tr></thead><tbody><tr><td>

Update Sets

</td><td>

Storing changes to a base system or installed application.Storing and applying a particular version of an application.

 Producing a file for export.

</td><td>

You can manually create update sets to store a particular application version.Use update sets to deploy patches or changes to installed applications.

 **Note:** Don’t use update sets to install applications. Instead, use the application repository or the ServiceNow Store to install applications.

</td></tr><tr><td>

Application Repository

</td><td>

Installing and updating applications on all company instances. Automatically managing application update sets.

 Restricting access to applications to the same company.

 Deploying completed applications to end users.

</td><td>

Consider uploading an application to the ServiceNow Store to share it with other users.

 Allows installation of and update to the latest application version only.

 Use update sets to store prior application versions.

 **Note:** If used with team development, publish applications only from a parent instance.

</td></tr></tbody>
</table>## Plan the update process

Before working with update sets, create a standard process for moving customizations from instance to instance using this check list:

1.  Check that both instances are on the same version. Customizations may not work if they rely on code that has changed between versions.
2.  Determine the changes to make in a single update set. Complete your update sets as you finish small to medium-sized tasks. As update sets get larger, it becomes harder to review them, takes longer to identify changes within them, increases the risk of conflicts with other update sets, and takes more time to preview and commit them. This is especially true if the update sets contain schema changes or revisions to large workflows or if the set has to be backed out.
3.  Confirm that all base system records have matching sys\_id fields. Some base system records are created on an instance after provisioning and don’t match between different instances, leading to problems with update sets. The best way to avoid this issue is to:
    -   Provision production and non-production instances.
    -   Clone the production instance onto the non-production instance.
4.  Identify a common path for update sets to move from instance to instance and maintain that model. Never migrate the same update set from multiple sources. Move update sets from dev to test and then from test to production.
5.  Plan for when to commit the update sets to production. Avoid committing an update set to a production instance during business hours. The instance may perform more slowly while the update set applies. Rest assured, this slower performance is temporary.
6.  Make sure update set names are clear. Create a naming convention to coordinate changes from multiple developers and to reference when committing the changes to another instance.
    -   If update sets are being generated as fixes for problems, consider including the problem ticket in the name \(for example, **PR10005 - Duplicate Email Issues Fix**\).
    -   If you need more than one update set to address a problem, include a sequence number in the naming convention. Doing so helps ensure that update sets are applied in the order that they were created \(for example, **PR10005 - Duplicate Email Issues Fix** and **PR10005.2 - Duplicate Email Issues Fix**\).
7.  Understand the following about update sets:
    -   What records are generated.
    -   Which customizations are tracked.
    -   Which dictionary changes are valid.
    -   Which customizations can be backed out \(reversed\) after applied.
8.  Before making any customizations, double-check that the correct update set is selected.

## Working with update sets

Review this information to avoid errors and performance issues.

-   Don’t delete update sets. If an update set is deleted, any updated records may be overwritten in the next update.
-   Don’t include the **system\_id** field from the ldap\_server\_config record in an update set. An update set from a working configuration points to the wrong system\_id node for the target instance and doesn’t work.
-   Don’t back out the Default update set. This action damages the system.
-   Never change the **Update Set** field value \(update\_set\) in a Customer Update record \(sys\_update\_xml\). If a customization is made in the wrong update set, take the following action:
    1.  Switch to the desired update set.
    2.  Modify the object \(record\) that was originally changed. You can make a trivial change, such as adding a field.
    3.  Save the record.
    4.  Back out the change just performed, and then save the record again.

        This action ensures that the latest version of the object is included in the desired update set and prevents duplicate updates for the same object in a single update set.

-   Don’t mark an update set as **Complete** until it’s ready to migrate. After an update set is complete, don’t change it back to **In progress**. Instead, create another update set for the rest of the changes, and make sure to commit them together in the order that they were created. Naming conventions may help in this case \(for example, Performance Enhancements and Performance Enhancements 2\).
-   Don’t manually merge updates into an update set. Use the Merge Update Sets module. This tool compares duplicate files between update sets and selects the newest version.
-   If a committed update set has a problem in the test instance, build the fix in another update set in the development instance. Commit this set to the test instance, and then make sure both sets are migrated to the production instance and committed in the order they were made.
-   Always preview an update set before committing it.
-   Set completed update set on the production instance to **Ignore**. This state ensures the update set isn’t reapplied when cloning the instance.
-   Keep a to-do list of manual changes and data loads that must be completed after an update set is applied.
-   Don’t make too many changes at one time. Verify that the correct changes have been made incrementally.
-   You can’t change a single update to update across multiple domains \(that is, global and TOP domains\). This function isn’t supported in the ServiceNow AI Platform.

To create an update set see [Create and select an update set as the current set](../task/create-select-update-set.md).

