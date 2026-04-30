---
title: Activate Service Portal validation scripts
description: Validate user input in a specific field type using a validation script. In new instances, Service Portal includes XML, Script, Script \(Plain\), Email, and Version validation scripts by default. If upgrading from a previous release, the Mobile and Service Portal version is not active by default. You must activate the Mobile and Service Portal version of the validation script to validate user input in the Service Portal.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Upgrading Service Portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Activate Service Portal validation scripts

Validate user input in a specific field type using a validation script. In new instances, Service Portal includes XML, Script, Script \(Plain\), Email, and Version validation scripts by default. If upgrading from a previous release, the Mobile and Service Portal version is not active by default. You must activate the Mobile and Service Portal version of the validation script to validate user input in the Service Portal.

## Before you begin

Role required: admin

## About this task

Service Portal requires that the **UI Type** field be set to **All** or **Mobile / Service Portal**. Client Scripts marked as **Desktop** rely on legacy APIs that are not supported in Service Portal. Before flagging a script as Mobile / Service Portal or All, make sure you are only using supported client-side APIs. See [Supported client script types and APIs](../reference/client-script-reference.md).

**Note:** To change the UI Type from **Mobile / Service Portal** to **All**, delete the Desktop version from your instance to avoid activating conflicting scripts. Before deleting the Desktop version, make a backup in case you need to revert any changes.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Validation Scripts**.

2.  Open the Mobile / Service Portal version of the validation script you would like to use in the Service Portal.

3.  Click the **Active** flag to activate the validation script.

4.  Set the UI Type to **All** to use the validation script in desktop, mobile, and Service Portal environments.

    To avoid activating conflicting validation scripts, you must first delete the Desktop version of the script.

    1.  Navigate to the desktop version of the validation script you would like to replace.

        Desktop versions have the **UI Type** field set to **Desktop**.

    2.  Open the record.

    3.  Right-click the header menu and select **Export** &gt; **XML \(This Record\)** to create a backup of the record.

    4.  Once the export completes, click **Delete** and confirm the selection.

    5.  Navigate back to the validation script set to **Active** in earlier steps and change the **UI Type** to **All**.


## Result

User input into the designated field type in the Service Portal and Mobile environments is validated for correct formatting. For example, if you activated the Email validation script for use in the Service Portal, invalid user input into an Email field generates an error and prevents the browser from submitting the form.

**Note:** On a desktop browser, the field is validated when you submit the record. On a mobile browser, the field is validated when you navigate away from the field.

**Parent Topic:**[Upgrading Service Portal](upgrading-service-portal.md)

