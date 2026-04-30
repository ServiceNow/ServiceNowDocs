---
title: Verify the HashCode of a package version in RPA Hub
description: Verify the HashCode of a package version in RPA Hub so that you can validate the HashCode of the manually uploaded automation zip file with the associated package version record.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Verify the HashCode of a package version in RPA Hub

Verify the HashCode of a package version in RPA Hub so that you can validate the HashCode of the manually uploaded automation zip file with the associated package version record.

## Before you begin

You must do this task in the classic environment.

Ensure that you’ve completed the tasks that are related to migrating your data from a lower environment to a higher environment. For more information, see [Migrating your data from a lower environment to a higher environment in RPA Hub](../concept/migrate-data-rpa-hub.md).

Ensure that the **sn\_rpa\_fdn.allow\_manual\_upload\_of\_automation\_package** system property is marked as true. If you have the admin role, you can edit this system property.

Upload an automation package. For more information, see [Upload an automation package attachment in RPA Hub](upload-package-version-attach.md).

Verify that the life-cycle stage of the package version isn’t set to **Retired**.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

A HashCode is a unique, auto-generated alphanumeric value of a published package version that is used to validate the integrity of the package version. The system verifies the HashCode of the first attachment that is uploaded on the package version record. To ensure a successful validation, upload only the correct attachment.

Another way to verify the HashCode of a package version is via triggering the **Verify HashCode of a Package Version** Action in Workflow Studio. For more information, see [Workflow Studio actions and subflow in RPA Hub](../reference/rpa-hub-actions.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Build** &gt; **Packages**.

2.  Open a package to view the HashCode.

3.  On the **Package Versions** tab, select a version.

4.  In the form header, select **Verify Hash Code**.


## What to do next

If the HashCode validation fails, remove the invalid attachment and upload the correct automation package. For more information, see [Upload an automation package attachment in RPA Hub](upload-package-version-attach.md).

**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

