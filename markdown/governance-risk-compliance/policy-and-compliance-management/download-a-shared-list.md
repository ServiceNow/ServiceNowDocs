---
title: Download a UCF shared list
description: In order for compliance managers to download UCF authority documents from the UCF CCH, the list must be marked as Shared. When updating Authority Documents or adding new ones, you must update all your authority documents to ensure that the common controls framework remains in sync with the authority documents you are using.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [integrate with UCF Common Controls Hub, Configure UCF integration using UCF CCH, Manage UCF integration, Classic UI, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Download a UCF shared list

In order for compliance managers to download UCF authority documents from the UCF CCH, the list must be marked as Shared. When updating Authority Documents or adding new ones, you must update all your authority documents to ensure that the common controls framework remains in sync with the authority documents you are using.

## Before you begin

Role required: sn\_compliance.admin or sn\_compliance.manager

**Note:** The current design of UCF supports the downloading of mandated and implied controls. The downloading of implementation controls is not supported. See the Unified Compliance Documentation [How do I distribute an authority document list to other accounts?](https://support.commoncontrolshub.com/hc/en-us/articles/208151063-How-do-I-Distribute-an-Authority-Document-List-to-other-Accounts-).

All data imported from UCF Authority Documents is read-only and must be protected. Do not customize the authority documents, citations, or control objectives on any UCF fields on the GRC tables.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Unified Compliance Integration**.

2.  Click the **UCF** configuration.

3.  [Configure the UCF integration using the UCF Common Controls Hub](configure-UCF-integration.md), if necessary.

4.  Click **Import Shared List**.

    A progress bar shows the progress of downloading and importing the documents.

    ![Download complete shown](../image/ucf-download-complete.png)

    You may encounter any of the following errors:

<table id="table_jdb_xkg_n1b"><thead><tr><th>

Error

</th><th>

Explanation

</th><th>

Resolve

</th></tr></thead><tbody><tr><td>

Error encountered while downloading UCF content. Try again or contact your system administrator for further assistance.

</td><td>

If the internet connection is lost for any reason, this message appears.

</td><td>

Click **Import Shared List** to download again.

</td></tr><tr><td>

Error encountered while downloading UCF content. Try again or contact your system administrator for further assistance.

</td><td>

This message may also indicate that the authority documents are part of an existing shared list or a possibility of a UCF import error. It suggests that you review the validity of the authority documents, citations, control objectives, and the links to the mapping of citation and control objectives.

</td><td>

Starting with Policy and Compliance Management version 12.0.4, your UCF Administrator receives an email with links to any invalid records. 1.  Click a link in the mail and fix the record\(s\) listed.
2.  Repeat for other invalid records, if they appear in the email.
3.  Click **Import Shared List** to download again.
 **Note:**

A system property called **sn\_comp\_ucf.deactivate\_deprecated\_docs** controls whether an email notification is sent when invalid or deprecated records are encountered during a shared list import. The property defaults to true. Set the property as false if you are downloading UCF content in multiple shared list. When the property is set as false the documents are not deprecated but an email is sent.

</td></tr><tr><td>

The selected Shared List does not match the existing Authority Document list. Select a different Shared List or update the existing Shared List.

</td><td>

If the selected UCF Shared List that you are downloading does not include all the authority documents you have already downloaded, this message appears.

</td><td>

1.  Return to the CCH and verify that the Shared List you are trying to download includes all the Authority Documents from the original import to your instance.
2.  Click **Import Shared List** to download again.


</td></tr></tbody>
</table>5.  Click **Review Changed Records** to review the list of changed records.

    ![List of changed records](../image/ucf-review-records.png)

    Authority documents in the UCF content are organized and mapped to their proper citations, which in turn are mapped to a common set of controls. The terminology between UCF and the GRC applications differs slightly as explained in the following table.

    |UCF|ServiceNow GRC application|
    |---|--------------------------|
    |Authority Document|Authority Document|
    |Citation|Citation|
    |Control|Control objective|


**Parent Topic:**[Integrate with UCF Common Controls Hub to manage compliance frameworks](../concept/c_UCF.md)

