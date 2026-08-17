---
title: Firewall rule requests
description: Use Service Catalog to request new firewall policies and rules.Request one or more firewall rules using Service Catalog to manage various IP addresses and enhance network security and accommodate evolving business requirements.Approval of firewall requests gives you controlled access and compliance. Members of the approver group can review and approve firewall audits and new firewall requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/firewall-requests.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Firewall rule requests

Use Service Catalog to request new firewall policies and rules.

\[Omitted image "request\_new\_firewall.png"\] Alt text: Request new firewall rule

**Parent Topic:**[Using Firewall Audits and Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/firewall-audit-report-use.md)

## Request firewall rule

Request one or more firewall rules using Service Catalog to manage various IP addresses and enhance network security and accommodate evolving business requirements.

### Before you begin

Verify that the Firewall Audits and Reporting catalog is enabled.

Role required: firewall\_admin

### About this task

You can request multiple firewall rule configurations in a single request. The system creates one parent firewall task with individual configuration tasks for each rule. Administrators initiate tasks, which are automatically directed to the risk team for assessment and approval. Following approval, firewall admins smoothly implement changes, all orchestrated through automated workflows.

**Note:** Starting with version 1.12.0 of Firewall Audits and Reporting, all new firewall rule tasks are created in the Panorama-specific table and display the task type as Panorama. Open requests created before version 1.12.0 are read-only. To proceed with those requests, resubmit them using the current catalog form.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Firewall Rules**.

2.  Select **Request Firewall Rule**.

    \[Omitted image "request\_firewall\_form.png"\] Alt text: Request firewall form.

3.  Enter the appropriate information for the following mandatory fields.

4.  -   Source IP address
-   Destination IP address
-   Assignment Group

    Must have the **sn\_disco\_firewall.firewall\_user** role.

-   Approval Group

    Must have the **approver\_user** role.

5.  Enter or select any details that is required.

6.  To add additional rule configurations, select **Add Rule Config** and enter the details for each additional rule.

    Each rule configuration you add creates a separate configuration task under the same parent firewall task. All configurations share the common fields such as Assignment Group and Approval Group.

7.  Select **Submit**.

    The system creates one parent firewall rule task with individual configuration tasks for each rule you specified.


### What to do next

To verify the new rule task, navigate to **Rule Requests** &gt; **Rule Requests Task**. Your request appears in the list with the task type set to Panorama. Open the parent task to view all individual rule configuration tasks.

## Approve firewall requests

Approval of firewall requests gives you controlled access and compliance. Members of the approver group can review and approve firewall audits and new firewall requests.

### Before you begin

Role required: Members of the specified approver group **approval\_group** specified in the rule task. The admin user can edit the approvers list in the Rule Request Task.

### Procedure

1.  Navigate to **All** &gt; **Self Service** &gt; **My Approvals**.

2.  Select the green checkmark to approve.


### Result

-   The Assignment group works on the request and marks it as **Close Complete**.
-   Once the assignment\_group marks the request **Close Complete**, if the change request plugin is activated, a background sub-flow creates a change request.

    **Note:** The change request is created only if the rule task is **Approved** and in **Close Complete** state.


The Firewall rule task security policy M2M corresponds to the related list **Security policies** in **Rule task**. Firewall administrators can add **description** or **tag** fields in a security policy on a Panorama device. They can also add firewall rule task numbers or change request numbers while creating or modifying security policies on Panorama. When the next discovery runs, the M2M table populates the mapping between:

-   Firewall rule task and firewall security policy
-   Firewall security policy and business service if the business service is provided during the Firewall rule task request

