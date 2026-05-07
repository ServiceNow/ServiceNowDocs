---
title: Defining Approval Rule for Outbound Intel
description: Define approval rules to control whether certain users require approval before sharing the shared intelligence.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Outbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Defining Approval Rule for Outbound Intel

Define approval rules to control whether certain users require approval before sharing the shared intelligence.

## Before you begin

Role required: sn\_sec\_tisc.admin

You can configure approval rules on the Outbound Intel record. These rules determine if a sharing requires approval based on the user roles or other criteria.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Administration** icon on the workspace.

3.  Go to **Outbound Intel Sharing**.

4.  Select **Approval Rule for Outbound Intel**.

    **Note:** Within the base system, the **Approval Rule for Outbound Intelligence** is the default rule provisioned within the base system to activate the approval workflow.

    The approval rule is applicable to only on-demand outbound intelligence sharing. For more information on on-demand outbound intelligence, see. [Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md).

5.  On the approval rule form, enter at least one user or user group in each of the following sections:

    1.  **Select User or Groups requiring approval**

    2.  **Select approver\(s\)**

6.  Click on **Enable** button to enable the approval flow for the Inbound Intel.

    **Note:**

    -   Once enabled, any applicable Outbound Intel record will be routed to the approval queue.
    -   The assigned approver\(s\) will review the changes made by the analyst and choose to either approve or reject the request.
    -   After a decision is made, an email notification is sent to the user\(s\) or user group\(s\), indicating whether the record has been approved or rejected.

**Parent Topic:**[Exploring Outbound Intel Sharing](../concept/tisc-outbound-intel-sharing.md)

**Related topics**  


[Configuring Outbound Intel Sharing Controls](tisc-outbound-sharing.md)

[Configuring Outbound Intel Data Exclusion Rule](tisc-outbound-data-exclusion.md)

[Configuring Outbound Intel Sharing Profiles](tisc-outbound-sharing-profiles.md)

[Configuring Outbound Intel Sharing Groups](tisc-config-inbound-sharing-groups.md)

[Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md)

[Working on the Redaction Library](tisc-redaction-library.md)

