---
title: Computer Telephony Integration in Service Operations Workspace
description: Service Operations Workspace provides an agent \(with the sn\_openframe\_user role\) to receive inbound calls and place outbound calls using the Computer Telephony Integration \(CTI\) interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/configure-cti-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Computer Telephony Integration in Service Operations Workspace

Service Operations Workspace provides an agent \(with the sn\_openframe\_user role\) to receive inbound calls and place outbound calls using the Computer Telephony Integration \(CTI\) interface.

The OpenFrame window is available to agents with the following roles.

-   sn\_openframe\_user
-   sn\_customerservice\_agent
-   sn\_customerservice.consumer\_agent
-   admin

After getting the required role, CTI must be enabled in the Service Operations Workspace by the admin. For more information about enabling CTI in the Service Operations Workspace, see [Enable Computer Telephony Integration providers to interact with the Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/integrate-cti-sow.md).

After the CTI integration, the agent can call a user using the phone number in the user profile and contact cards through any of these options:

**Note:**

The application’s default CTI windows in the following images are provided for demo purposes only.

Ensure that your instance contains the required connectors for communication.

-   Record information from the contextual side panel of a record.

    \[Omitted image "record-info-cti.png"\] Alt text: Agent making a CTI call from record information.

-   On-call escalation.

    \[Omitted image "on-call-escalation-cti.png"\] Alt text: Agent making a CTI call from an on-call escalation.


**Parent Topic:**[Managing IT services in your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/managing-services-operations-in-organization.md)

**Related topics**  


[Knowledge Management in Service Operations Workspace]()

[Major Incident Management in Service Operations Workspace]()

[On-Call Scheduling in Service Operations Workspace]()

[Problem Management in Service Operations Workspace]()

[Recommendation Framework in Service Operations Workspace]()

[Recommended Actions for ITSM in Service Operations Workspace]()

[ServiceNow integrations with Microsoft Teams in Service Operations Workspace]()

[Service Level Management in Service Operations Workspace]()

[Walk-up Experience management in Service Operations Workspace]()

[Collaboration in Service Operations Workspace]()

[Universal Request in Service Operations Workspace]()

[Universal Task in Service Operations Workspace]()

[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace]()

