---
title: Create a change request in the Remediation view
description: From a remediation task \(VUL, AVUL, CVUL, or CRG\), create a change request. Alternatively, add a remediation task to an existing change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/sem-ws-CRs.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 2
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Create a change request in the Remediation view

From a remediation task \(VUL, AVUL, CVUL, or CRG\), create a change request. Alternatively, add a remediation task to an existing change request.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

**Note:** The itil role is required if you want to submit change requests from the Remediation view.

## About this task

For more information about the change requests and creating change requests from the classic environment, see [Change management for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-response/vuln-change_mgmnt_ovrvw.md).

**Note:** The **Create Change** and **Add to existing change** options are available only when the ITSM Advanced plugin is enabled on your instance. If you have migrated to an ITSM AI Native SKU without ITSM Advanced, upgrade to ITSM Advanced SKU to restore access.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **Remediation**.

2.  Open a remediation task \(VUL, AVUL, CVUL, or CRG\) that you want to create a change request for.

3.  Select **Create Change** to create a change request.

    1.  Fill in the fields on the change request form.

        For information on the form fields, see [Create change request form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/it-remediation-workspace/itr-ws-create-cr-fields.md).

    2.  Select **Create Change Request**.

4.  To add this remediation task to an existing change request instead, expand the **Create Change** button and select **Add to existing change**.

    1.  Select the search icon to view the list of existing change requests.

        -   You can filter the list using the filter icon and the **Advanced view** condition builder.
        -   To include configuration items from all active vulnerable items in the change request, select the **Add CIs to CR** check box.
    2.  Select a change request from the list.

    3.  Select **Add change**.


## Result

The remediation task record opens and a message indicates that the change request is created or the remediation task is added to an existing change request.

-   Select the **View change** link in the message to open the change request \(CHG\) record.
-   Select the **Change Requests** related item menu link on the remediation task record to view all the change requests associated with the record.

When you submit the change and it is implemented, if state synchronization is enabled, the remediation task automatically moves to `Resolved`. For more information about states and state synchronization in change requests, see [Create a change request from a remediation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-response/vuln-change_mgmnt_create_change.md).

**Parent Topic:**[Using Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/using-unified-security-exposure-management.md)

