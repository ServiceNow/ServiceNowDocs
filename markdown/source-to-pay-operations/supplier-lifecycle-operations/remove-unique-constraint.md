---
title: Remove the unique constraint from Email Domain
description: Multiple supplier records can have the same email domain after removing the unique constraint from the Email Domain column of the Supplier Email Domain \[sn\_slm\_email\_domain\] table.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-11-25"
reading_time_minutes: 1
breadcrumb: [Enable M2M mapping between supplier contact and suppliers, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Remove the unique constraint from Email Domain

Multiple supplier records can have the same email domain after removing the **unique** constraint from the `Email Domain` column of the Supplier Email Domain \[sn\_slm\_email\_domain\] table.

## Before you begin

Role required: admin

**Important:** This procedure is required only for the upgrade scenarios \(for all earlier versions upgrading to the Xanadu December 2024 release\).

## Procedure

1.  In the navigation filter, enter **sn\_slm\_email\_domain\_list.do**.

2.  Hover and right-click **Email Domain** field to open the Dictionary Entry of `sn_slm_email_domain` table.

    ![Email domain dictionary view of the sn_slm_email_domain table](../image/email-domain.png)

3.  Select the form context menu icon \(![Context menu icon](../image/context-menu.png)\) and select **Configure** &gt; **Form Layout**.

4.  From the **Available** list of fields, select the **Unique** field and move it to the **Selected** column.

5.  Select **Save**.

    The **Unique** field is now available in the Dictionary of the `sn_slm_email_domain` table.

6.  Navigate to the Dictionary of `sn_slm_email_domain` table, clear the **Unique** check box and save the form.

    **Note:** If you are still unable to invite a supplier contact with duplicate domain, or if the onboarding playbook is stuck while waiting to send out an email to the supplier contact, follow the troubleshooting steps in the KB article [KB1709872](https://support.servicenow.com/kb?sys_kb_id=43cccf6483ca9a10cdbbc430feaad3d4&id=kb_article_view).


**Parent Topic:**[Enable M2M mapping between supplier contact and suppliers](enable-m2m-supplier-contacts.md)

