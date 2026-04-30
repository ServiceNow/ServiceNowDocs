---
title: Save an update set as a local XML file
description: Administrators can export an update set as an XML file to save a specific version of an application or set of changes.Administrators can load an update set XML file to apply a specific version of an application or set of changes.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working with update sets, System update sets, Deploying applications, Building applications]
---

# Save an update set as a local XML file

Administrators can export an update set as an XML file to save a specific version of an application or set of changes.

## Before you begin

Role required: admin

## About this task

Typically you create an XML file of an update set when one of the following conditions apply:

-   The two instances do not have network connectivity so you cannot retrieve update sets from the remote instance nor create a data source to pull, or import, data directly from the source instance.
-   You do not want to provide administrator credentials to the source instance \(for example, you do not want to share an administrator password with people outside your company\) so you cannot retrieve update sets nor create a data source.
-   You want to back up important customizations locally.

The ability to export and import customizations as an XML file is provided by the following UI Actions:

-   **Export to XML** on the Update Set \[sys\_update\_set\] table.
-   **Export to XML** on the Retrieved Update Set \[sys\_remote\_update\_set\] table.
-   **Import Update Set from XML** on the Retrieved Update Set \[sys\_remote\_update\_set\] table.

The **Export to XML** UI Action on Update Set \[sys\_update\_set\] table calls a processor called UnloadRetrievedUpdateSet, which transforms a local update set into a retrieved update set, exports the retrieved update set with its related list, and then deletes the temporary update set, if necessary.

Both **Export to XML** UI actions depend on the script include ExportWithRelatedLists, which exports a record and manually defined related lists to a single XML file.

## Procedure

1.  Navigate to **System Update Sets** and click either **Local Update Sets** or **Retrieved Update Sets**.

    **Note:** **Retrieved Update Sets** must be in a loaded state to be exported.

2.  Select an update set that is in the **Complete** state.

3.  On the Update Set form, click the **Export to XML** Related Link.

4.  Save the XML file.

    An XML file is created. When the file is uploaded to another instance, it appears as a retrieved update set regardless of whether it is local or retrieved on the instance where it is created.


**Parent Topic:**[Working with update sets](../concept/using-system-update-sets.md)

## Load customizations from a single XML file

Administrators can load an update set XML file to apply a specific version of an application or set of changes.

### Before you begin

Roles required: admin

### Procedure

1.  Elevate privileges to the security\_admin role.

2.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

3.  Click the link **Import Update Set from XML**.

4.  Click **Choose File** and select an XML file.

5.  Click **Upload**.

    The customization is now available as a retrieved update set with state Loaded.

6.  Follow standard procedure to commit the update set.

    ![Retrieved update set](../image/LoadUpdateSetFromXML.png "Retrieved update sets")


