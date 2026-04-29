---
title: Submit an IoC Lookup request from a security incident
description: An IoC lookup automatically runs whenever observables are added to a security incident. Also, if your security incident has attachments, they can be easily found with the press of a button.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage lookups and scans, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit an IoC Lookup request from a security incident

An IoC lookup automatically runs whenever observables are added to a security incident. Also, if your security incident has attachments, they can be easily found with the press of a button.

## Before you begin

For automatic IoC lookups, the Threat Intelligence plugin must be activated.

Role required: sn\_si.basic

**Note:** By default, the **Lookup Type** for **File** is inactive.

## Procedure

1.  [Create a new security incident](t_ManuallyCreateSecurityIncident.md) or open an existing one if you intend to attach new files to it.

2.  Click the paperclip icon in the form header and attach one or more files.

3.  When you have completed your entries on the form, right-click the form header and click **Save**.

    After the record has been saved, a **Lookup attachments** button appears.

4.  Click **Lookup attachments**.

    **Note:** The work notes under **Incident Details** report the progress of the lookup process.

5.  You can click the lookup number at the end of the message to view the lookup record.

    You can click the Lookup reference link to view detailed results.

    ![Lookup request message](../image/LookupRequestFromSI.png)


