---
title: Configuring contextual security for the list editor
description: The list editor enforces existing access control rules \(ACLs\) and additional security controls to restrict editing from a list.
locale: en-US
release: zurich
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [List editor, Administer, List administration, Forms, fields, and lists, Configure core features, Administer]
---

# Configuring contextual security for the list editor

The list editor enforces existing access control rules \(ACLs\) and additional security controls to restrict editing from a list.

The list\_edit security operation specifically controls the ability to edit information in a list. Apply this operation in the same manner as the write operation to limit list editing for fields that require the user to navigate to the form. Reasons you may require a user to edit a field in a form include complex UI policy constraints or other policies you have in place.

-   write and list\_edit access to the field
-   write and list\_edit access to any dependent fields of the field
-   write and list\_edit access to any fields that depend on the field being edited

To configure access controls, navigate to **System Security** &gt; **Access Controls**. The following examples use the list\_edit security operation to restrict list editing in certain contexts.

