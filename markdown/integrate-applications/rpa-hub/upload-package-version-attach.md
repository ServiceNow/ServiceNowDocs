---
title: Upload an automation package attachment in RPA Hub
description: Upload a zip file of the automation package in RPA Hub to manually migrate the package from a lower \(non-production\) to a higher \(production\) environment.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Upload an automation package attachment in RPA Hub

Upload a zip file of the automation package in RPA Hub to manually migrate the package from a lower \(non-production\) to a higher \(production\) environment.

## Before you begin

You must do this task in the classic environment.

Ensure that you’ve completed the tasks that are related to migrating your data from a lower environment to a higher environment. For more information, see [Migrating your data from a lower environment to a higher environment in RPA Hub](../concept/migrate-data-rpa-hub.md).

Download the package version attachment from a lower instance. For more information, see [Download a package version in RPA Hub](download-package-version.md).

Ensure that the **sn\_rpa\_fdn.allow\_manual\_upload\_of\_automation\_package** system property is marked as true. If you have the admin role, you can edit this system property.

Verify that the life-cycle stage of the package version isn’t set to **Retired**.

Ensure that there’s no valid attachment that is associated with the package version record.

For a quick integrity check, verify that the HashCode of a package version is correct. If the validation fails, remove the incorrect attachment that you previously uploaded by selecting **Manage Attachments**. Then, proceed with this task to upload a correct attachment. For more information about verifying the HashCode, see [Verify the HashCode of a package version in RPA Hub](view-hash-code.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager

## About this task

You can upload the valid attachment only one time. The **Upload Attachment** button to upload attachments is turned off after you upload a valid attachment.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Build** &gt; **Packages**.

2.  Open a package that you want to upload a package version for.

3.  On the **Package Versions** tab, select a version.

4.  In the form header, select **Upload Attachment** to upload a zip file of the automation package.

5.  In the Confirmation dialog box, select **Choose file**.


## What to do next

For a quick integrity check, verify the HashCode of a package version again. For more information, see [Verify the HashCode of a package version in RPA Hub](view-hash-code.md).

**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

