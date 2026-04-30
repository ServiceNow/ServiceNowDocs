---
title: Components installed with Cloud Account Management
description: Several user roles are installed with the Cloud Account Management app.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2024-04-18"
reading_time_minutes: 1
breadcrumb: [Cloud Account Management reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Components installed with Cloud Account Management

Several user roles are installed with the Cloud Account Management app.

## Roles installed

<table id="table_dgb_ppt_cbc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Group that provides the role

</th></tr></thead><tbody><tr><td>

Requester\[sn\_itom\_cam.cw\_requester\]

</td><td>

Team lead or representative of the application.-   Initiates cloud account creation requests.
-   Create requests for suspension or reactivation of their own accounts.

</td><td>

ITOM CAM Requester Group

</td></tr><tr><td>

Approver\[sn\_itom\_cam.cw\_approver\]

</td><td>

Supervisor, manager, or finance approver.Reviews requests and either approves or denies them.

</td><td>

ITOM CAM Approver Group

</td></tr><tr><td>

Admin\[sn\_itom\_cam.cw\_admin\]

</td><td>

Cloud Center of Excellence \(CCOE\) or Sites Reliability Engineer \(SRE\) team member.-   Confirms that Cloud Account Management configurations align with the cloud and Terraform configurations.
-   Customizes the data certification policy.
-   Creates accounts that are outside the Cloud Account Management application.

</td><td>

ITOM CAM Admin Group

</td></tr><tr><td>

Certifier

 \[sn\_itom\_cam.cw\_certifier\]

</td><td>

Marks an account as certified or failed.

</td><td>

ITOM CAM Certifier Group

</td></tr></tbody>
</table>To return to the main topic, see [Exploring Cloud Account Management](../concept/exploring-cam.md).

**Parent Topic:**[Cloud Account Management reference](cam-reference.md)

