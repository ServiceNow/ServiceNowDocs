---
title: Retrieve an update set
description: Retrieve completed update sets from another instance.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with update sets, System update sets, Deploying applications, Building applications]
---

# Retrieve an update set

Retrieve completed update sets from another instance.

## Before you begin

Role required: admin or teamdev\_user

**Warning:** Update sets let you transfer changes across instances with different family releases and features. You can load update sets from older releases into newer ones, but loading updates from newer releases into older instances may cause errors or data loss and should be avoided if possible. The same cautions apply when moving updates between different versions of store apps.

## Procedure

1.  If IP address access control is enabled on the source instance, set up the target instance as an exception.

2.  On the target instance, navigate to **System Update Sets** &gt; **Update Sources** and select **New**.

3.  Specify the connection settings as described in the table.

<table id="table_zpq_zbw_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the instance.

</td></tr><tr><td>

Type

</td><td>

Specify whether the remote instance is a development, test, or UAT instance.

</td></tr><tr><td>

Active

</td><td>

Specify whether the local instance can transfer update sets to the remote instance. You can transfer update sets only to active remote instances.

</td></tr><tr><td>

URL

</td><td>

Specify the URL of the remote instance using the appropriate transfer protocol. Each remote instance record should have a unique URL. Creating duplicate records with the same URL can cause errors. The remote instance must be on the same release family as the local instance.

 **Note:** You can’t change the URL after the system verifies the connection. Use the Active field to deactivate unwanted remote instances.

</td></tr><tr><td>

Username

</td><td>

Enter the user on the remote instance who authorizes transferring update sets to the instance. This user account must have the admin user role on the remote instance.

</td></tr><tr><td>

Password

</td><td>

Enter the password of the authorizing user.

</td></tr><tr><td>

Short description

</td><td>

Enter any other relevant information about the remote instance.

</td></tr></tbody>
</table>4.  Select **Test Connection**.

    If the connection is successful, a confirmation message appears. If the connection fails, a warning message identifies the cause of the failure.

5.  If the connection fails, modify the settings to establish connectivity.

    Connectivity must be established prior to saving the connection settings. Additionally, it may be necessary to modify the source instance configuration, such as updating the password.

6.  Select and hold \(or right-click\) the form header and select **Save**.

7.  Under **Related Links**, select **Retrieve Completed Update Sets**.

    Update sets marked as completed are moved from the source to the target instance, while existing update sets on the target are skipped. The confirmation page details how many sets were transferred and skipped.

8.  To view retrieved update set, navigate to **System Update Sets** &gt; **Retrieved Update Sets**.


**Parent Topic:**[Working with update sets](../concept/using-system-update-sets.md)

