---
title: Computer Telephony Integration in Service Operations Workspace
description: Service Operations Workspace provides an agent \(with the sn\_openframe\_user role\) to receive inbound calls and place outbound calls using the Computer Telephony Integration \(CTI\) interface.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Computer Telephony Integration in Service Operations Workspace

Service Operations Workspace provides an agent \(with the sn\_openframe\_user role\) to receive inbound calls and place outbound calls using the Computer Telephony Integration \(CTI\) interface.

The OpenFrame window is available to agents with the following roles.

-   sn\_openframe\_user
-   sn\_customerservice\_agent
-   sn\_customerservice.consumer\_agent
-   admin

After getting the required role, CTI must be enabled in the Service Operations Workspace by the admin. For more information about enabling CTI in the Service Operations Workspace, see [Enable Computer Telephony Integration providers to interact with the Service Operations Workspace](../task/integrate-cti-sow.md).

After the CTI integration, the agent can call a user using the phone number in the user profile and contact cards through any of these options:

**Note:**

The application’s default CTI windows in the following images are provided for demo purposes only.

Ensure that your instance contains the required connectors for communication.

-   Record information from the contextual side panel of a record.

    ![Agent making a CTI call from record information.](../image/record-info-cti.png "CTI call from record information")

-   On-call escalation.

    ![Agent making a CTI call from an on-call escalation.](../image/on-call-escalation-cti.png "CTI call from an on-call escalation")


**Parent Topic:**[Managing IT services in your organization](managing-services-operations-in-organization.md)

**Related topics**  


[Knowledge Management in Service Operations Workspace](knowledge-articles-sow.md)

[Major Incident Management in Service Operations Workspace](mim-in-sow.md)

[On-Call Scheduling in Service Operations Workspace](on-call-scheduling-in-sow.md)

[Problem Management in Service Operations Workspace](problem-sow.md)

[Recommendation Framework in Service Operations Workspace](recommendation-framework-sow.md)

[Recommended Actions for ITSM in Service Operations Workspace](recommended-actions-for-itsm-in-service-operations-workspace.md)

[ServiceNow integrations with Microsoft Teams in Service Operations Workspace](msteams-sow.md)

[Service Level Management in Service Operations Workspace](slm-sow.md#)

[Walk-up Experience management in Service Operations Workspace](walkup-sow.md)

[Collaboration in Service Operations Workspace](collaboration-sow.md)

[Universal Request in Service Operations Workspace](using-ur-sow.md)

[Universal Task in Service Operations Workspace](using-ut-sow.md)

[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace](resetting-password-pr-sow.md)

