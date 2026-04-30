---
title: Auto populate information from email to legal request or matter
description: Map the sender's email address, email content, and subject field from an email to legal request fields to automatically fill in information from the email to the submitted legal request.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Outlook Add-In for Legal Service Delivery, Microsoft Outlook Add-In for Legal Service Delivery, Integration of Legal Service Delivery with third-party applications, Legal Service Delivery, Employee Service Management]
---

# Auto populate information from email to legal request or matter

Map the sender's email address, email content, and subject field from an email to legal request fields to automatically fill in information from the email to the submitted legal request.

## Before you begin

Role required: sn\_lg\_ops.legal\_config

## About this task

The script include **OutlookMappingConfig** available in the base system supports the mapping of the following variables of the email.

-   *subject* - Subject of the email.
-   *fromEmail* - Sender's email address.
-   *body* - Email content

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Select the **OutlookMappingConfig**.

3.  In the **Script** field, specify the mappings.

<table id="choicetable_phr_kxb_gzb"><thead><tr><th align="left" id="d200368e111">

Variables from email

</th><th align="left" id="d200368e114">

Variables from legal request

</th></tr></thead><tbody><tr><td id="d200368e120">

**subject**

</td><td>

Specify the legal request variable into which you want to store the email subject line.

Example: If you want to copy the subject of email into the short description of the legal request, map *subject* with *short\_description* by including the following code.```
short_description: "subject"
```

</td></tr><tr><td id="d200368e140">

**fromEmail**

</td><td>

Specify the legal request variable into which you want to store the sender's email address.

Example: If you want to copy the sender's email address into the requested for of the legal request, map *fromEmail* with *requested\_for* by including the following code.```
requested_for: "fromEmail"
```

</td></tr></tbody>
</table><table id="choicetable_mdk_wvs_xcc"><thead><tr><th align="left" id="d200368e163">

Variables from email

</th><th align="left" id="d200368e166">

Variables from legal request

</th></tr></thead><tbody><tr><td id="d200368e172">

**subject**

</td><td>

Specify the legal request variable into which you want to store the email subject line.

Example: If you want to copy the subject of email into the short description of the legal request, map *subject* with *short\_description* by including the following code.```
short_description: "subject"
```

</td></tr><tr><td id="d200368e192">

**fromEmail**

</td><td>

Specify the legal request variable into which you want to store the sender's email address.

Example: If you want to copy the sender's email address into the requested for of the legal request, map *fromEmail* with *requested\_for* by including the following code.```
requested_for: "fromEmail"
```

</td></tr><tr><td id="d200368e214">

**body**

</td><td>

Specify the legal request variable into which you want to store the email content.

Example: If you want to copy email content into the description, map *body* with *description* by including the following code.```
description: "body"
```

</td></tr></tbody>
</table>
**Parent Topic:**[Configure Microsoft Outlook Add-In for Legal Service Delivery](../concept/lsd-outlook-addin-configure.md)

