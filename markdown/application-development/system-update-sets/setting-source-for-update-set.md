---
title: Set up the source instance for an update set
description: Set up the source instance for an update set.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-08-01"
reading_time_minutes: 1
breadcrumb: [Transfers, System update sets, Deploying applications, Building applications]
---

# Set up the source instance for an update set

Set up the source instance for an update set.

## Before you begin

Role required: admin

## Procedure

1.  If IP address access control is enabled on the source instance, set up the target instance as an exception.

2.  On the target instance, navigate to **System Update Sets** &gt; **Update Sources** and select **New**.

3.  Specify the connection settings as described in the table.

<table id="table_qtl_sq3_2gc"><thead><tr><th>

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

Specify the URL of the remote instance using the appropriate transfer protocol. Each remote instance record should have a unique URL. Creating duplicate records with the same URL can cause errors. The remote instance must be on the same release family as the local instance. **Note:** You can’t change the URL after the system verifies the connection. Use the Active field to deactivate unwanted remote instances.

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

\[Optional\] Enter any other relevant information about the remote instance.

</td></tr></tbody>
</table>4.  Select **Test Connection**.

    -   If the connection is successful, a confirmation message appears.
    -   If the connection fails, a warning message identifies the cause of the failure.
5.  If the connection fails, modify the settings to establish connectivity.

    -   You must establish connectivity before you can save the connection settings.
    -   You must modify the source instance \(for example, change the password\).
6.  Select and hold \(or right-click\) the form header and select **Save**.


