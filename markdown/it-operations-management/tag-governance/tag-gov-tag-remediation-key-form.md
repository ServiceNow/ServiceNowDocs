---
title: Tag Remediation Key form
description: You use the Tag Remediation Key form to create a tag remediation key.
locale: en-US
release: australia
product: Tag Governance
classification: tag-governance
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tag Governance reference, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Tag Remediation Key form

You use the Tag Remediation Key form to create a tag remediation key.

<table id="table_rtn_p42_kmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key

</td><td>

Tag key value that is used to remediate non-compliant CIs. For example, if the remediation preview shows the value as `cost center`, you can specify `cost center` as a new remediation key if it doesn't exist.

</td></tr><tr><td>

Order

</td><td>

Order of execution that the system considers when you initiate remediation. For example, you can run a tag count policy for four tags and identify CIs that are missing two tag keys. If you've configured multiple remediation keys, the system considers the two keys with the lowest values in the order field.

</td></tr><tr><td>

Remediation

</td><td>

Remediation name and record preview.

</td></tr><tr><td>

Value Type

</td><td>

Type of the value that you specify in the **Value** field — **Static** or **String**. Based on your selection, you must specify a script or a value for the tag key.

</td></tr><tr><td>

Value

</td><td>

String value for the key that you're creating.This field appears only when **String** is selected in the **Value Type** field.

</td></tr><tr><td>

Script

</td><td>

Script code to generate values for the key. This field appears only when **Script** is selected in the **Value Type** field.

</td></tr></tbody>
</table>**Parent Topic:**[Tag Governance reference](../concept/reference-tag-governance.md)

