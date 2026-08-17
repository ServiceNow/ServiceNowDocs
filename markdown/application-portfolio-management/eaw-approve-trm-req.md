---
title: Approve or reject TRM requests
description: As an Enterprise Architect, approve or reject a TRM product or product lifecycle requests submitted by other users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-approve-trm-req.html
release: australia
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 2
breadcrumb: [Working with Technology Reference Model \(TRM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Approve or reject TRM requests

As an Enterprise Architect, approve or reject a TRM product or product lifecycle requests submitted by other users.

## Before you begin

The user must be part of the Enterprise Architect Group.

Role required: sn\_apm.apm\_analyst

## About this task

When an Enterprise Architecture user submits a TRM product request or a TRM product lifecycle request, the Enterprise Architect group receives an email notification.

A TRM product request can include one or more associated lifecycle requests. The product request record displays the requested lifecycles in the **Requested Lifecycles** tab and any existing lifecycles for the same product in the **Existing Lifecycles** tab.

A standalone TRM product lifecycle request can include multiple child lifecycle records submitted in a single bulk request. The parent lifecycle request record shows all child lifecycle records in the **Requested Lifecycles** tab. Approving or rejecting the parent request determines the outcome for all associated child lifecycle records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  In the Needs Attention section, select the **My Approvals** tab.

3.  Select a request number to open it.

    The Approvals list includes both TRM product requests \(TRMPREQ\) and TRM product lifecycle requests \(TRMLCREQ\).

4.  Review the request details and the associated lifecycle records.

    -   Select the **Requested Lifecycles** tab to view the lifecycle records included in this request. Each lifecycle record shows the version, edition \(for software products\) or hardware model \(for hardware products\), requested TRM phase, and phase start and end dates.
    -   Select the **Existing Lifecycles** tab to view any lifecycles already on the product to help you identify potential conflicts before approving.
5.  Select **Approve** or **Reject**.

    Edit the request details such as **Requested TRM phase**, **Category**, and **Business Justification** before approving, if needed. Select **Update** to save edits without triggering an approval decision.


## Result

-   When a TRM product request is approved, the TRM product and all associated lifecycle records are created in the system simultaneously. The requester receives an email notification.
-   When a standalone TRM product lifecycle request is approved, all child lifecycle records in the request are created and linked to the parent product. The requester receives an email notification.
-   When a request is rejected, no product or lifecycle records are created. The requester receives an email notification.

**Parent Topic:**[Working with Technology Reference Model \(TRM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-trm.md)

**Related topics**  


[View or update your TRM requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-update-trm-requests.md)

[Manage the Technology Reference Model in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-managing-the-technology-portfolio.md)

