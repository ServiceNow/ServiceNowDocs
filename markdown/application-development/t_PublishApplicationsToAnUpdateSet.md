---
title: Publish an application to an Update Set
description: Publishing an application creates an update set containing the current version of all application configuration records.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Publish an application to an Update Set

Publishing an application creates an update set containing the current version of all application configuration records.

## Before you begin

Role required: admin, or delegated\_developer with Publish To Update Set permission enabled

## About this task

You can use this update set as a backup file for auditing purposes or to transfer the application to another instance.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company's Applications**.

2.  Click the **In Development** tab.

3.  Open the application record you want to create an update set for.

4.  Click the **Publish to Update Set** related link.

5.  Fill in the fields, as appropriate \(see table\).

    ![Publish to Update Set](../image/PublishToUpdateSet.png)

<table id="table_cr1_2yy_sr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application name

</td><td>

\[Read-only\] Displays the name of the application that you are publishing.

</td></tr><tr><td>

Version

</td><td>

Enter version information to append to the Update Set name in dot-notation such as 1.2.3. The platform saves the information you enter here in the application **Version** field.

 The Update Set has the name &lt;Application name&gt; - &lt;Version&gt;. If you leave this field blank, the initial Update Set has the name &lt;Application name&gt; and subsequent Update Sets have the name &lt;Application name&gt; - &lt;Sequential number&gt;.

</td></tr><tr><td>

Description

</td><td>

Enter a description for the Update Set. By default, this field contains the short description of the application.

</td></tr><tr><td>

Include data

</td><td>

Select the check box to include a limited number of data records from each table in the application. Use this feature to package sample data with your applications.

 **Warning:**

Using this feature to migrate large quantities of data records between instances can cause performance issues, as it is not intended for this purpose. To migrate data, use an instance-to-instance import. You can adjust the maximum number of data records to include with an application.

See [Import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/c_ImportSetsKeyConcepts.md).

 -   If your sample data includes tables with record numbering, the current counter value is also transferred. When the update set is applied on another instance, the counter is set to the larger of the sample data or the target instance counter.
-   For translated fields, only records in English are transferred.


</td></tr></tbody>
</table>6.  Click **Publish**.

    A new update set is created and the latest update of each application file in the application is copied into it. The update set is marked as complete.

7.  Transfer the update set to another instance according to your test process.

    -   Retrieve the update set from the source instance.
    -   Save the update set as an XML file.
8.  Run any fix scripts that are included in the application.


**Parent Topic:**[Application sharing](../concept/c_SharingApplications.md)

**Related topics**  


[Retrieve an update set](../../system-update-sets/task/t_RetrieveAnUpdateSet.md)

[Save an update set as a local XML file](../../system-update-sets/task/t_SaveAnUpdateSetAsAnXMLFile.md#)

[Run fix scripts](t_RunFixScripts.md)

[Delegate development and deployment permissions to personnel](t_AddADeveloper.md)

