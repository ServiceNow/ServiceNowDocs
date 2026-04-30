---
title: Using e-signature template for non-HR tasks
description: Create or modify an e-signature template to define an electronic document and signature configuration for use in non-HR task forms.
locale: en-US
release: zurich
product: e-Signature
classification: e-signature
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using e-signature, E-signature, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using e-signature template for non-HR tasks

Create or modify an e-signature template to define an electronic document and signature configuration for use in non-HR task forms.

## Before you begin

Role required: sn\_esign.admin or sn\_esign.config\_manager

## Procedure

1.  Create an e-sign template on the required task table \(for example, Incident\).

    See [Create or modify an e-signature template](configure-e-signature-configuration.md). Select **Managed Document** in **Document type** and **Signature** in **E-signature type**.

2.  Configure the task form \(for example, Incident form\) by adding the **E-Signature Template** field.

3.  Configure the related lists on the task form by adding E-signature history.

4.  Select the e-sign template that you have created in the **Template** field.

5.  Assign a group and a user to the task.

    To retrieve the signature log, navigate to **System Logs** &gt; **Signature Images \(signature\_image table\)**. Also, you can view the E-signature history in the related list.


## What to do next

When a user receives the task and moves the task to Work in Progress state, the **Sign document** option is available for the user to sign the document.

**Parent Topic:**[Using e-signature](../concept/using-esignature.md)

