---
title: Firewall rule requests
description: Use Service Catalog to request new firewall policies and rules.Request a new firewall rule using the Service Catalog to manage various IP addresses, enhance network security, and accommodate evolving business requirements.Approval of firewall requests gives you controlled access and compliance. Members of the approver group can review and approve firewall audits and new firewall requests.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Firewall Audits and Reporting, Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Firewall rule requests

Use Service Catalog to request new firewall policies and rules.

![Request new firewall rule](../image/request_new_firewall.png "Firewall rule request workflow")

**Parent Topic:**[Using Firewall Audits and Reporting](firewall-audit-report-use.md)

## Request new firewall rule

Request a new firewall rule using the Service Catalog to manage various IP addresses, enhance network security, and accommodate evolving business requirements.

### Before you begin

Ensure that the Firewall Audits and Reporting catalog is enabled.

Role required: firewall\_admin

### About this task

Administrators initiate tasks, which are automatically directed to the risk team for assessment and approval. Following approval, firewall admins implement these changes through automated workflows.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Firewall Rules**.

2.  Select **Request Firewall Rule**.

    ![Request firewall form.](../image/request_firewall_form.png "Request Firewall Rule")

3.  Enter the appropriate information for the following mandatory fields:

4.  -   Source IP address
-   Destination IP address
-   Assignment Group

    Must have the **sn\_disco\_firewall.firewall\_user** role.

-   Approval Group

    Must have the **approver\_user** role.

5.  Enter or select any required details.

6.  Select **Submit**.

    The firewall rule task is created.


### What to do next

Verify the new rule task. Navigate to **Rule Requests** &gt; **Rule Requests Task**. Your request should be visible in the list.

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

