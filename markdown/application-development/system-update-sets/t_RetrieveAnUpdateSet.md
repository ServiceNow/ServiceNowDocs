---
title: Retrieve an update set
description: Retrieve completed update sets from another instance.
locale: en-US
release: yokohama
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Update set transfers, System update sets, Deploying applications, Building applications]
---

# Retrieve an update set

Retrieve completed update sets from another instance.

## About this task

**Warning:** Update sets allow moving changes between instances that may be running different family release versions and different features. You can always load an update set created on an older family release on an instance running a newer family release. Loading an update set created on a newer family release on an instance running an older family release requires additional testing to determine compatibility. Updates from newer family releases may not produce the same functionality when moved to older family releases. In extreme cases, newer family release updates may cause outages or data loss on an older family release instance. Where possible, avoid moving updates from newer family releases to older family releases. Similar constraints apply to moving updates between instances running different versions of ServiceNow Store apps.

## Procedure

1.  If IP address access control is enabled on the source instance, set up the target instance as an exception.

2.  On the target instance, navigate to **System Update Sets** &gt; **Update Sources** and click **New**.

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

 **Note:** You cannot change the URL after the system verifies the connection. Use the Active field to deactivate unwanted remote instances.

</td></tr><tr><td>

Username

</td><td>

Enter the user on the remote instance who authorizes transferring update sets to this the instance. This user account must have the admin user role on the remote instance.

</td></tr><tr><td>

Password

</td><td>

Enter the password of the authorizing user.

</td></tr><tr><td>

Short description

</td><td>

\[Optional\] Enter any other relevant information about the remote instance.

</td></tr></tbody>
</table>4.  Click **Test Connection**.

    -   If the connection is successful, a confirmation message appears.
    -   If the connection fails, a warning message identifies the cause of the failure.
5.  If the connection fails, modify the settings to establish connectivity.

    -   You must establish connectivity before you can save the connection settings.
    -   You may want to modify the source instance \(for example, change the password\).
6.  Right-click the form header and select **Save**.

7.  Under **Related Links**, click **Retrieve Completed Update Sets**.

    -   Any update sets marked as **Completed** are transferred from the source instance to the target instance. Update sets that already exist on the target instance are skipped.
    -   The confirmation page provides detailed messages about how many update sets were transferred and how many were skipped.
    -   To view retrieved update set, navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

## What to do next

If the system property **glide.update\_set.auto\_preview** is set to **true**, the system automatically starts the preview process after the update set is retrieved. If this property is **false**, you must start the process manually. For more information on the preview process, see [Preview a remote update set](t_PreviewARemoteUpdateSet.md#).

