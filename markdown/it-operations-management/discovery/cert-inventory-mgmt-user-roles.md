---
title: Certificate Inventory and Management roles and responsibilities
description: Dedicated users with specialized roles are assigned to optimize the monitoring and tracking of requests for new and renewing certificates.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Inventory and Management roles and responsibilities

Dedicated users with specialized roles are assigned to optimize the monitoring and tracking of requests for new and renewing certificates.

The Certificate Inventory and Management dashboard and certificate configuration settings are activated or deactivated depending on the assigned roles.

<table id="table_o1v_pbq_31c"><thead><tr><th>

Role

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

Certificate Administrator \[sn\_disco\_certmgmt.pki\_admin\]

</td><td>

The headless user \(an account not tied to a specific user\) is included in the base system and equipped with the **sn\_disco\_certmgmt.pki\_admin** role. It serves as the caller for automatically generated renewal certificate tasks and incidents. To customize this user, adjust the user ID using the Discovery property: **glide.discovery.certs.cert\_admin\_user\_id** instead of leaving it as the default headless user.

 Responsible for changing non-standard attributes in the original certificate record, this role can modify attributes like state, status, assigned to, assignment group, renewal tracking, and service type. The certificate's inherent attributes remain unaltered. The default state for discovered certificates is installed, but this role can manually adjust it to other states such as issued, installed, revoked, and retired. Additionally, users with this role have the capability to view diverse dashboards and possess read/write access to certificates and certificate tasks associated with certificate Discovery.

 **Note:**

-   The sn\_disco\_certmgmt.pki\_admin role contains the sn\_disco\_certmgmt.pki\_user role.
-   Any user with the pki\_admin role can be added to the approver field in the certificate request form. Users with pki\_admin role should be assigned with the approval\_admin role manually to approve or reject requests from the certificate task form. This approver does not need to login to approve the task. In a certificate task form or related list, system admin or a user with approval\_admin role or pki\_admin role can add multiple approvers or edit the existing one.
-   The approver\_user role is required if the user wants to approve a request by logging in. Without the approver\_user role, a user doesn't have the option to navigate to **My Approvals** where the requests can be approved.

</td></tr><tr><td>

Certificate User\[sn\_disco\_certmgmt.pki\_user\]

</td><td>

Responsible for overseeing certificate discovery, this role is granted the ability to access diverse dashboards and has read/write permissions for certificates and associated certificate tasks.

</td></tr><tr><td>

Certificate Approver \[sn\_disco\_certmgmt.pki\_approver\]

</td><td>

Responsible for certificate requests, a user with this role \(normal user\) can initiate certificate requests through the Service Catalog form.

</td></tr><tr><td>

Certificate Requester\[sn\_disco\_certmgmt.certificate\_requester\]

</td><td>

Responsible for submitting certificate requests, this role is granted the ability to request and renew certificates from the Service Catalog.

</td></tr></tbody>
</table>