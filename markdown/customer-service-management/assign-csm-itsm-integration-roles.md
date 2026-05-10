---
title: Assigning CSM/ITSM integration roles
description: To enable the Service Management integration features, assign the CSM/ITSM integration roles that are included with the Incident Management application.Several types of roles are available with CSM integration with ITSM.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up CSM integration with IT Service Management, Integrate with IT Service Management, Integrate, Customer Service Management]
---

# Assigning CSM/ITSM integration roles

To enable the Service Management integration features, assign the CSM/ITSM integration roles that are included with the Incident Management application.

The Service Management integration plugins do not add any roles to the customer service agent role \(sn\_customerservice\_agent\). To enable the Service Management integration features, you must assign the CSM/ITSM integration roles included with the Incident Management application.

-   Assign roles to agents using guided setup. For more information, see [Integrate with IT Service Management using Guided Setup](configure-csm-sm-integration.md).
-   Assign roles to agents using the ServiceNow AI Platform user administration feature. For more information, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignARoleToAUser.md).

## CSM/ITSM integration roles

Several types of roles are available with CSM integration with ITSM.

### CSM/ITSM integration roles for agents

These roles enable customer service agents to view and create incident, problem, change, and request records for customer service cases.

<table id="table_xhr_dq2_hhb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_incident\_read

</td><td>

Customer service agents with this role can:-   View information about an incident record associated with a customer service case.
-   Associate an existing incident record with a customer service case.
-   Remove an incident record associated with a customer service case.

</td><td>

-   dependency\_views
-   workspace\_agent
-   view\_changer
-   sn\_comm\_management.comm\_plan\_viewer
-   cmdb\_read
-   cmdb\_query\_builder\_read

</td></tr><tr><td>

sn\_incident\_write

</td><td>

Customer service agents with this role can:-   Create an incident record for a customer services case.
-   Associate an existing incident record with a customer service case.
-   Remove an incident record associated with a customer service case.

</td><td>

sn\_incident\_read

</td></tr><tr><td>

sn\_problem\_read

</td><td>

Customer service agents with this role can:-   View information about a problem record associated with a customer service case.
-   Associate an existing problem record with a customer service case.
-   Remove a problem record associated with a customer service case.

</td><td>

-   dependency\_views
-   workspace\_agent
-   view\_changer
-   cmdb\_read
-   cmdb\_query\_builder\_read

</td></tr><tr><td>

sn\_problem\_write

</td><td>

Customer service agents with this role can:-   Create a problem record for a customer services case.
-   Associate an existing problem record with a customer service case.
-   Remove a problem record associated with a customer service case.

</td><td>

sn\_problem\_read

</td></tr><tr><td>

sn\_change\_read

</td><td>

Customer service agents with this role can:-   View information about a change record associated with a customer service case.
-   Associate an existing change record with a customer service case.
-   Remove a change record associated with a customer service case.

</td><td>

-   dependency\_views
-   workspace\_agent
-   view\_changer
-   cmdb\_read
-   app\_service\_user
-   cmdb\_query\_builder\_read

</td></tr><tr><td>

sn\_change\_write

</td><td>

Customer service agents with this role can:-   Create a change record for a customer services case.
-   Associate an existing change record with a customer service case.
-   Remove a change record associated with a customer service case.

</td><td>

-   sn\_change\_read
-   template\_editor
-   cmdb\_query\_builder

</td></tr><tr><td>

sn\_request\_read

</td><td>

Customer service agents with this role can view information about request records associated with a customer service case in the **Requests** related list.

</td><td>

None

</td></tr><tr><td>

sn\_request\_write

</td><td>

Customer service agents with this role can create request records for customer service cases.

</td><td>

-   sn\_request\_read
-   task\_editor
-   dependency\_views
-   workspace\_agent
-   view\_changer
-   cmdb\_read
-   cmdb\_query\_builder\_read

</td></tr></tbody>
</table>### CSM/ITSM integration roles for external customers

These roles enable external customers to take the following actions:

-   View and create request records from the Customer and Consumer Service Portals.
-   Approve changes and requests from the Customer Service Portal.

<table id="table_x3w_2d1_g3b"><thead><tr><th>

Role

</th><th>

Actions

</th></tr></thead><tbody><tr><td>

Customer administrator\[sn\_customerservice.customer\_admin\]

</td><td>

Users with this role can:-   Browse the service catalog and catalog items and make a selection.
-   Create requests for themselves, for other contacts from the same account, or for child accounts.
-   View the request details.

</td></tr><tr><td>

Partner\[sn\_customerservice.partner\]

</td><td>

Users with this role can:-   Browse the service catalog and catalog items and make a selection.
-   Create requests for themselves \(if they also have the customer role\).
-   Create requests on behalf of the accounts with which they have established relationships.
-   View cases and requests.

</td></tr><tr><td>

Customer case manager\[sn\_customerservice.customer\_case\_manager\]

</td><td>

Users with this role can:-   Browse the service catalog and catalog items and make a selection.
-   Create requests for themselves or for other contacts from the same account.
-   View the request details.

</td></tr><tr><td>

Customer\[sn\_customerservice.customer\]

</td><td>

Users with this role can:-   Create a request.
-   View the request details.

</td></tr><tr><td>

Proxy contact\[sn\_customerservice.proxy\_contact\]

</td><td>

Users with this role can:-   Browse the service catalog and catalog items and make a selection.
-   Create requests on behalf of customers.
-   Add the account and contact information of the customers.
-   View the details of the case and the related request.

</td></tr></tbody>
</table>