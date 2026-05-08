---
title: Auto populate information from email to legal request or matter
description: Map the sender's email address, email content, and subject field from an email to legal request fields to automatically fill in information from the email to the submitted legal request.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Outlook Add-In for Legal Service Delivery, Microsoft Outlook Add-In for Legal Service Delivery, Integration with Third-party applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
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

3.  Define the email mapping with the intake forms of the practice area.

    1.  Open the script include.

    2.  Copy and paste the existing mapping object into the script field.

    3.  Copy the sys\_id of the intake form of the practice area that you want to map to the email.

    4.  Replace the object key with the copied sys\_id.

        ![Defining the email mapping with the intake forms in the script include.](../image/defining-email-mapping-with-intake-forms.jpg)

4.  In the copied mapping object, specify the key-value pairs using the variables from the intake form.

<table id="choicetable_mdk_wvs_xcc"><thead><tr><th align="left" id="d229118e172">

Variables from email

</th><th align="left" id="d229118e175">

Variables from legal request

</th></tr></thead><tbody><tr><td id="d229118e181">

**subject**

</td><td>

Specify the legal request variable into which you want to store the email subject line.

Example: If you want to copy the subject of email into the short description of the legal request, map *subject* with *short\_description* by including the following code.```
short_description: "subject"
```

</td></tr><tr><td id="d229118e201">

**fromEmail**

</td><td>

Specify the legal request variable into which you want to store the sender's email address.

Example: If you want to copy the sender's email address into the requested for of the legal request, map *fromEmail* with *requested\_for* by including the following code.```
requested_for: "fromEmail"
```

</td></tr><tr><td id="d229118e221">

**body**

</td><td>

Specify the legal request variable into which you want to store the email content.

Example: If you want to copy email content into the description, map *body* with *description* by including the following code.```
description: "body"
```

</td></tr></tbody>
</table>5.  After defining the object, select **Update**.


**Parent Topic:**[Configure Microsoft Outlook Add-In for Legal Service Delivery](../concept/lsd-outlook-addin-configure.md)

