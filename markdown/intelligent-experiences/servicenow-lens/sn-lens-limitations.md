---
title: ServiceNow AI Lens limitations
description: Be aware of a few limitations when you’re using the ServiceNow AI Lens application.
locale: en-US
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow AI Lens, Enable AI experiences]
---

# ServiceNow AI Lens limitations

Be aware of a few limitations when you’re using the ServiceNow AI Lens application.

<table id="table_ptl_hjd_w2c"><thead><tr><th>

Limit

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum number of images

</td><td>

Maximum number of images that can be uploaded to ServiceNow AI Lens is 10.

</td></tr><tr><td>

Maximum character limit

</td><td>

In the instructions field for the analysis, you can enter up to 500 characters.

</td></tr><tr><td>

Themes

</td><td>

When you change the theme on the ServiceNow instance, the theme of the ServiceNow AI Lens is automatically updated. But, if you have already started a ServiceNow AI Lens session and then you change the theme on the instance, the theme doesn't change automatically until you launch a new session.This behavior is standard for the ServiceNow AI Platform.

</td></tr><tr><td>

Language

</td><td>

When you change the language on the ServiceNow instance, the language of the ServiceNow AI Lens is automatically changed. But, if you have already started a ServiceNow AI Lens session and then you change the language on the instance, the language doesn't change automatically until you launch a new session. This behavior is standard for the ServiceNow AI Platform.

When using ServiceNow AI Lens to scan non-English documents—such as invoices in Chinese— you may notice inconsistencies in translation, formatting, or data extraction. These discrepancies result from limitations in how the underlying LLM processes different locales.

</td></tr><tr><td>

Auto-fill

</td><td>

Pre-populated form fields, such as record number, can be overwritten by ServiceNow AI Lens. You must verify the auto-filled form fields before saving the form.

</td></tr><tr><td>

Visibility of the **Create with Lens** button

</td><td>

As a user with the lens\_user role, if you don’t have the Write access for the first record of any list, the **Create with Lens** button doesn't appear in the list view of the table. You can sort the records to show a different record on top and reload the list to view the **Create with Lens** button.

</td></tr><tr><td>

Hallucinations

</td><td>

If the large language model \(LLM\) returns text that doesn’t exist in the source artifacts, the LLM might inject out-of-context information. You must verify that all information aligns with the source material to ensure that there are no fabricated facts or unsupported conclusions.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Lens reference](servicenow-lens-reference.md)

