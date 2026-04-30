---
title: Import a package version attachment in RPA Hub
description: Import package version attachments automatically instead of manually uploading a package version attachment, by selecting the Import Attachment button on a package version.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Import a package version attachment in RPA Hub

Import package version attachments automatically instead of manually uploading a package version attachment, by selecting the **Import Attachment** button on a package version.

## Before you begin

Perform the following tasks before you import a package version attachment:

-   Ensure that you’ve completed the tasks that are related to migrating your data from a lower environment to a higher environment. For more information, see [Migrating your data from a lower environment to a higher environment in RPA Hub](../concept/migrate-data-rpa-hub.md).
-   Ensure that the **sn\_rpa\_fdn.allow\_manual\_upload\_of\_automation\_package** system property is marked as true. If you have the admin role, you can edit this system property.
-   Ensure that there is no valid attachment associated to the package version​.
-   Verify that the life-cycle stage of the package version isn’t set to **Retired**.
-   Create an active connection in the **RPA Automation Package** connection and credential alias. Ensure to provide the lower \(non-production\) environment in the **Connection URL** field. For more information, see [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

The maximum package size is determined by the **com.glide.attachment.max\_size** system property. For more information about this system property, [Maximum allowed attachment size \[Updated in Security Center 1.3\]](https://www.servicenow.com/docs/access?context=sc-max-allowed-attachment-size&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Perform this task if you are automatically migrating the package attachment \(automation zip file\) from a lower \(non-production\) to a higher \(production\) environment.

Another way to import package version attachments automatically is via triggering the **Import Package Version Attachment** Subflow in Workflow Studio. For more information, see [RPA Hub actions and subflow](../reference/rpa-hub-actions.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Packages**.

4.  Open a package whose package version you want to import.

5.  On the **Package Versions** tab, select a version that you want to import.

6.  Select **Import Attachment**.

7.  In the Confirmation dialog box, select **Import Attachment**.


## Result

After the attachment is uploaded successfully or if an error occurs while uploading the attachment, an email notification is sent to the user who performs this import attachment action.

## What to do next

For a quick integrity check, verify the HashCode of a package version again. For more information, see [Verify the HashCode of a package version in RPA Hub](view-hash-code.md).

**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

