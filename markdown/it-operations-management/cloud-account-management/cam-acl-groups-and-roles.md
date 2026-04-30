---
title: Cloud Account Management ACL groups, roles, and responsibilities
description: Access control lists \(ACLs\), groups, and roles in Cloud Account Management control how access permissions are organized and managed within a cloud environment.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2024-08-23"
reading_time_minutes: 2
breadcrumb: [Cloud Account Management reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Account Management ACL groups, roles, and responsibilities

Access control lists \(ACLs\), groups, and roles in Cloud Account Management control how access permissions are organized and managed within a cloud environment.

## Groups and roles in Cloud Account Management

<table id="table_p5t_vvg_fdc"><thead><tr><th>

Group

</th><th>

Role

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

ITOM Cloud Account Management requester group

</td><td>

sn\_itom\_cam.cw\_requester

</td><td>

-   Initiates cloud account requests: Triggers the process for creating cloud accounts.
-   Justifies account creation: Provides clear and compelling reasons for why each cloud account is needed.
-   Gathers and submits account information: Collects and submits all the necessary details required for successful cloud account creation.
-   Manages account status: Request suspension or reactivation of cloud accounts as needed.

</td></tr><tr><td>

ITOM Cloud Account Management approver group

</td><td>

sn\_itom\_cam.cw\_approver

</td><td>

-   Evaluates and approves account requests: Review account creation requests, carefully assessing their validity and alignment with budget constraints. Following this evaluation, the administrator grants approval or denial of the request.
-   Verifies budgetary compliance: Confirms that the requested cloud account aligns with available budgetary resources before granting approval.
-   Communicates decisions with clear rationale: Communicates clearly the approval or denial decision to the requester by adding a comment to the request itself. This comment should provide a concise and informative explanation for the decision.

</td></tr><tr><td>

ITOM Cloud Account Management admin group

</td><td>

sn\_itom\_cam.cw\_admin

</td><td>

-   Verifies configuration alignment: Verifies that Cloud Account Management configurations are consistent and aligned with both cloud provider configurations and Terraform configurations. This process promotes secure access management practices across all environments.
-   Provisions cloud accounts: Configures the cloud context to provision new cloud accounts, streamlining the account creation process.
-   Troubleshoots provisioning issues: Diagnoses and resolves any problems encountered during cloud account provisioning, promoting successful account creation.
-   Customizes data certification policy: Tailors the Cloud Account Management default data certification policy to meet specific organizational requirements, promoting appropriate data handling procedures.
-   Manages all accounts: Oversees all cloud accounts, including CW-managed accounts and on-boarded accounts, guaranteeing centralized control and visibility.

</td></tr><tr><td>

ITOM Cloud Account Management certifier group

</td><td>

sn\_itom\_cam.cw\_certifier

</td><td>

-   Certifies discovered accounts: Reviews discovered accounts listed in the Subscription Accounts tab and designates them as certified if they meet compliance standards or failed if they don't. This process verifies proper vetting and ongoing monitoring of cloud accounts.
-   Manages verification tasks: Accesses and reviews verification tasks associated with cloud accounts. Following review, the administrator can certify tasks to indicate their successful completion.

</td></tr></tbody>
</table>## How they work together

<table id="table_m2p_knd_ncc" class="collapse-folded"><thead><tr><th>

Group

</th><th>

Role

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

ITOM Cloud Account Management requester group

</td><td>

sn\_itom\_cam.cw\_requester

</td><td>

-   Initiates cloud account requests: Triggers the process for creating cloud accounts and provides the information for creating the account.
-   Manages account status: Requests suspension or reactivation of cloud accounts.

</td></tr><tr><td>

ITOM Cloud Account Management approver group

</td><td>

sn\_itom\_cam.cw\_approver

</td><td>

-   Evaluates and approves account requests.
-   Verifies budgetary compliance of requested cloud accounts and alignment with available budgetary resources.

</td></tr><tr><td>

ITOM Cloud Account Management certifier group

</td><td>

sn\_itom\_cam.cw\_certifier

</td><td>

-   Certifies discovered accounts.
-   Accesses and reviews verification tasks associated with cloud accounts.

</td></tr><tr><td>

ITOM Cloud Account Management admin group

</td><td>

sn\_itom\_cam.cw\_admin

</td><td>

-   Verifies that Cloud Account Management configurations are consistent and aligned with both cloud provider configurations and Terraform configurations.
-   Provisions cloud accounts.
-   Troubleshoots provisioning issues: Diagnoses and resolves any problems encountered during cloud account provisioning.
-   Customizes data certification policies to meet specific organizational requirements.
-   Oversees all cloud accounts, including CW-managed and on-boarded accounts, guaranteeing centralized control and visibility.

</td></tr></tbody>
</table>To return to the main topic, see [Exploring Cloud Account Management](../concept/exploring-cam.md).

**Parent Topic:**[Cloud Account Management reference](cam-reference.md)

