---
title: Setting up CSM integration with IT Service Management
description: Integrate Customer Service Management with IT Service Management that includes the Request, Incident, Problem, and Change Management applications. With this integration, users can create request, incident, problem, and change records from customer service cases. External users can view these records from the Customer and Consumer Service Portals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/setting-up-csm-integration-with-itsm.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate with IT Service Management, Integrate, Customer Service Management]
---

# Setting up CSM integration with IT Service Management

Integrate Customer Service Management with IT Service Management that includes the Request, Incident, Problem, and Change Management applications. With this integration, users can create request, incident, problem, and change records from customer service cases. External users can view these records from the Customer and Consumer Service Portals.

<table id="table_sqn_y5f_nlb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Integrate with IT Service Management using Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/configure-csm-sm-integration.md)

</td><td>

Use the Guided Setup to integrate CSM with IT Service Management.

</td></tr><tr><td>

[Activate Customer Service Management with Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/activate-csm-sm-integration.md)

</td><td>

Activate the CSM with Service Management plugin \(com.sn\_cs\_sm\) to enable the integration the following applications:

-   Incident Management
-   Problem Management
-   Change Management

</td></tr><tr><td>

[Activate Customer Service Management with Request Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/activate-csm-rm-integration.md)

</td><td>

Activate the CSM with Request Management plugin \(com.sn\_cs\_sm\_request\) to use the integration with the Request Management application.

</td></tr><tr><td>

[Assigning CSM/ITSM integration roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/assign-csm-itsm-integration-roles.md)

</td><td>

Assign the required roles to the customer service agents and managers who will be creating the request, incident, problem, and change records from customer service cases.

</td></tr><tr><td>

[Enable external customers to access problem, change, and request records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-itsm-integration-view-request.md)

</td><td>

Assign access controls \(ACLs\) to the external user roles to provide visibility to case-related request, problem, and change records from the Customer and Consumer Service Portals.

</td></tr><tr><td>

[Enable external customers to create requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/enable-customer-request-from-portal.md)

</td><td>

Assign roles to external customers which enable them to create requests.

</td></tr><tr><td>

[Enable external customers to approve requests and changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/enable-customer-request-approval.md)

</td><td>

Enable external customers to approve changes and requests:-   Add external users to approval groups or assign roles for approval users.
-   Add the necessary ACLs to the snc\_external role for the following table:
    -   Change Request \(change\_request\)
    -   Request \(sc\_request\)
    -   Request Item \(sc\_req\_item\)

</td></tr><tr><td>

[Enable the Create Request UI action for case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/enable-create-request-case-type.md)

</td><td>

Enable the **Create Request** UI action for case type tables that extend the Case \[sn\_customerservice\_case\] table.

</td></tr></tbody>
</table>