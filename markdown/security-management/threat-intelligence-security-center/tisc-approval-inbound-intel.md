---
title: Defining Approval Rule for Inbound Intel
description: Define approval rules to control whether certain profiles or groups require approval before processing the inbound intelligence.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Inbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Defining Approval Rule for Inbound Intel

Define approval rules to control whether certain profiles or groups require approval before processing the inbound intelligence.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select **Administration** icon on the workspace.

3.  Go to **Inbound Intel Sharing**.

4.  Select **Approval Rule for Inbound Intelligence**.

    **Note:** Within the base system, the **Approval Rule for Inbound Intelligence** is the default rule provisioned to activate the approval workflow.

5.  On the approval rule form, enter at least one user or user group in each of the following sections:

    1.  **Select profile or group for approval**: Under this section, select the Inbound Intel sharing profiles or Inbound intelligence sharing groups that requires approval for processing the inbound intelligence data.

    2.  **Select approver\(s\)**: Under this section, select the users or groups that are required to approve the inbound intelligence records received from the profiles/groups configured earlier.

6.  Select **Enable** button to enable the approval rule for the Inbound Intel.

    **Note:**

    -   Once enabled, any applicable Inbound Intel record will be routed to the approval queue.
    -   One or more assigned approvers review the changes made by the analyst and choose to either approve or reject the request.
    -   After a decision is made, an email notification is sent to email addresses as configured in the corresponding inbound intelligence sharing profile, indicating whether the record has been approved or rejected.

**Parent Topic:**[Exploring Inbound Intel Sharing](../concept/tisc-inbound-intel-sharing.md)

**Related topics**  


[Configuring Inbound Intel Sharing Profiles](tisc-config-inbound-profile.md)

[Configuring Inbound Intel Sharing Groups](tisc-config-inbound-groups.md)

