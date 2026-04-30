---
title: Administering form annotations
description: Form annotations are additional pieces of information on a form, such as a line or paragraph of text. Use form annotations to provide on-screen instructions to your users.You can store multiple translations of form annotation text.You can define the form annotation types to control their appearance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, Form administration, Forms, fields, and lists, Configure core features, Administer]
---

# Administering form annotations

Form annotations are additional pieces of information on a form, such as a line or paragraph of text. Use form annotations to provide on-screen instructions to your users.

Form annotations are enabled by default in the base system. To disable them, set the `glide.ui.form_annotations` system property to false.

**Parent Topic:**[Administering forms on the ServiceNow AI Platform](form-administration.md)

## Support multiple languages for a form annotation

You can store multiple translations of form annotation text.

### Before you begin

Role required: admin

### About this task

To support multiple languages, use [message records](../../localization/reference/r_MessageTable.md) to translate annotation text.

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Messages**.

2.  Create a message record for each language you support.

3.  On the Message form, set the **Key** field to a unique identifier for the annotation text.

    The annotation text is a good key. The key must be the same for each translation message for the annotation.

4.  Select the appropriate **Language**.

5.  In the **Message** field, enter the translated annotation text.

6.  Edit the form annotation and reference the message key with a gs.getMessage call.

    For example, if the message key is **Message key text**, enter`${gs.getMessage("Message key text")}` in the form annotation.


## Administer form annotation types

You can define the form annotation types to control their appearance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Form Annotation Types**.

2.  Set the **Active** field to **false** for any types you do not want to use.

3.  Click **New** to add a type.


