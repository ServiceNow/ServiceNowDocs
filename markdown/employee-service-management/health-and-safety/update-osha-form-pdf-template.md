---
title: Update an OSHA form PDF template
description: Update a saved OSHA form PDF template if changes to an OSHA form PDF file are required.
locale: en-US
release: zurich
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure settings, Health and Safety Incident Management OSHA Content Pack, Health and Safety injury and illness reports, Health and Safety, Employee Service Management]
---

# Update an OSHA form PDF template

Update a saved OSHA form PDF template if changes to an OSHA form PDF file are required.

## Before you begin

Role required: sn\_ohs\_im.admin or sn\_ohs\_im.agent

## About this task

PDF templates for OSHA forms are required to fill and export OSHA forms for safety incidents and the injuries and illnesses that happened in your organization.

The Health and Safety Incident Management OSHA Content Pack includes preconfigured PDF templates and associated sys\_ids for OSHA 300, 300A, and 301 forms. However, if changes to the OSHA form PDF files are needed, they can be updated.

## Procedure

1.  Upload the new OSHA form PDF template file.

    1.  Select **All**.

    2.  In the navigation filter, enter `sn_hs_im_osha_template.list` and press the Enter key.

        The HS OSHA PDF template \[sn\_hs\_im\_osha\_template\] table opens and a list of all the available PDF templates for OSHA forms appears.

    3.  Select the template that you need to update.

    4.  Select **Manage attachments** and delete the old PDF template file and upload the new PDF template file.

        For more information on managing attachments, see [Manage attachments](https://www.servicenow.com/docs/access?context=t_ManagingAttachments&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    5.  Select **Update**.

2.  Activate the uploaded OSHA form PDF template file and copy its sys\_id.

    1.  Select **All**.

    2.  In the navigation filter, enter `sys_attachment.list` and press the Enter key.

    3.  In the list, select the PDF template file attachment that you uploaded in step 1.

    4.  Set its **State** value as Available.

    5.  Right-click the PDF template file attachment and select **Copy sys\_id**.

3.  Update the sys\_id of the OSHA form PDF template file in the corresponding system property.

    1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

    2.  Select the corresponding system property for the OSHA form PDF template that you updated.

        For information on the OSHA form PDF template system properties, see [Health and Safety Incident Management OSHA Content Pack properties](../reference/properties-installed-osha-content-pack.md).

    3.  Update the sys\_id that you copied in step 2.

    4.  Select **Save**.


## Result

The new OSHA form PDF template is available and is used when exporting the corresponding OSHA form.

**Parent Topic:**[Setting up the OSHA Content Pack](../concept/configuring-osha-forms.md)

