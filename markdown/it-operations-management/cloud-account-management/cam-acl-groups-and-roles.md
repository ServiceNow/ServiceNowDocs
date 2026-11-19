---
title: Cloud Account Management ACL groups, roles, and responsibilities
description: Access control lists \(ACLs\), groups, and roles in Cloud Account Management control how access permissions are organized and managed within a cloud environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/cam-acl-groups-and-roles.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Account Management ACL groups, roles, and responsibilities

Access control lists \(ACLs\), groups, and roles in Cloud Account Management control how access permissions are organized and managed within a cloud environment.

<table id="table_m2p_knd_ncc" class="collapse-folded"><thead><tr><th>

Group

</th><th>

Role

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

ITOM Cloud Account Management requester group

</td><td>

**sn\_itom\_cam.cw\_requester**

</td><td>

-   Initiates cloud account requests: Triggers the process for creating cloud accounts and provides the information for creating the account.
-   Manages account status: Requests suspension or reactivation of cloud accounts.

</td></tr><tr><td>

ITOM Cloud Account Management approver group

</td><td>

**sn\_itom\_cam.cw\_approver**

</td><td>

-   Evaluates and approves account requests.
-   Verifies budgetary compliance of requested cloud accounts and alignment with available budgetary resources.

</td></tr><tr><td>

ITOM Cloud Account Management certifier group

</td><td>

**sn\_itom\_cam.cw\_certifier**

</td><td>

-   Certifies discovered accounts.
-   Accesses and reviews verification tasks associated with cloud accounts.

</td></tr><tr><td>

ITOM Cloud Account Management asset viewer group

</td><td>

**sn\_itom\_cam.cw\_asset\_viewer**

</td><td>

-   Views cloud account details and associated asset information.
-   Accesses read-only dashboards and reports for cloud accounts.

</td></tr><tr><td>

ITOM Cloud Account Management account manager group

</td><td>

**sn\_itom\_cam.account\_manager**

</td><td>

-   Manages the full lifecycle of cloud accounts, including creation, modification, and decommissioning.
-   Monitors account health and compliance across managed cloud environments.

</td></tr><tr><td>

ITOM Cloud Account Management admin group

</td><td>

**sn\_itom\_cam.cw\_admin**

</td><td>

-   Verifies that Cloud Account Management configurations are consistent and aligned with both cloud provider configurations and Terraform configurations.
-   Provisions cloud accounts.
-   Troubleshoots provisioning issues: Diagnoses and resolves any problems encountered during cloud account provisioning.
-   Customizes data certification policies to meet specific organizational requirements.
-   Oversees all cloud accounts, including CW-managed and on-boarded accounts, guaranteeing centralized control and visibility.

</td></tr></tbody>
</table>To return to the main topic, see [Exploring Cloud Account Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/exploring-cam.md).

**Parent Topic:**[Cloud Account Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/cam-reference.md)

