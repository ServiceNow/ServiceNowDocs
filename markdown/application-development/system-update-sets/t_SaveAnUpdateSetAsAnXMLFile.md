---
title: Save an update set as a local XML file
description: Administrators can export an update set as an XML file to save a specific version of an application or set of changes.Administrators can load an update set XML file to apply a specific version of an application or set of changes.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, System update sets, Deploying applications, Building applications]
---

# Save an update set as a local XML file

Administrators can export an update set as an XML file to save a specific version of an application or set of changes.

## Before you begin

Role required: admin

## About this task

Create an XML file of an update set when:

-   The two instances lack network connectivity, preventing the retrieval of update sets or the creation of a data source for import from the source instance.
-   You don't want to give administrator credentials for the source instance.
-   You want to back up important customizations locally.

## Procedure

1.  Navigate to **System Update Sets** and select either **Local Update Sets** or **Retrieved Update Sets**.

    **Note:** **Retrieved Update Sets** must be in a loaded state to be exported.

2.  Select an update set that is in the **Complete** state.

3.  On the Update Set form, select the **Export to XML** Related Link.

4.  Save the XML file.

    When a file is uploaded to a different instance, it’s recognized as a retrieved update set.


**Parent Topic:**[Configuring System Update Sets](../concept/configure-system-update-sets.md)

## Load customizations from a single XML file

Administrators can load an update set XML file to apply a specific version of an application or set of changes.

### Before you begin

Roles required: admin

### Procedure

1.  Elevate privileges to the security\_admin role.

2.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

3.  Select **Import Update Set from XML**.

4.  Select **Choose File** and select an XML file.

5.  Select **Upload**.

    The customization is available as a retrieved update set with the state **Loaded**.

6.  To commit the update set, see [Commit an update set](t_CommitAnUpdateSet.md).


