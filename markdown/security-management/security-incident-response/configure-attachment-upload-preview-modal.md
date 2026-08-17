---
title: Configure the preview modal for attachment upload
description: Configure whether the preview modal appears when security analysts attach files to a security incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/configure-attachment-upload-preview-modal.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
breadcrumb: [View and update Security Incident Response system properties, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure the preview modal for attachment upload

Configure whether the preview modal appears when security analysts attach files to a security incident record.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Security Incident Response Workspaces** &gt; **Administration**.

2.  Select **SIR Workspace Properties**.

3.  On the SIR Workspace Properties page, select **sn\_si\_aw.attachment.show\_preview\_modal**.

4.  On the sn\_si\_aw.attachment.show\_preview\_modal page, update the **Value** field to true or false.

    **Note:** By default, the **Value** field is set to false, and files upload directly without displaying a preview modal. To display the upload preview modal, set the **Value** field to true. If attachment encryption is enabled, this property is ignored and the upload preview modal always opens, regardless of the property's value.

5.  Select **Save**.


**Parent Topic:**[View and update Security Incident Response system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/view-update-sirw-system-properties.md)

