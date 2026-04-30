---
title: Supported and unsupported roles and features
description: Explore the capabilities and limitations of the unified consumer role \(sn\_customerservice.unified\_consumer\) to understand the roles and features it supports. This analysis helps you can enhance the user experience and streamline administration, supporting a unified identity across different user contexts.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring a user as a Unified Consumer, Configuring a Unified User, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Supported and unsupported roles and features

Explore the capabilities and limitations of the unified consumer role \(sn\_customerservice.unified\_consumer\) to understand the roles and features it supports. This analysis helps you can enhance the user experience and streamline administration, supporting a unified identity across different user contexts.

<table id="table_ijx_tjq_vzb"><thead><tr><th>

Supported or unsupported

</th><th>

Persona and role \[Role Name\]

</th><th>

Internal role\(s\)

</th><th>

External role\(s\)

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Supported

</td><td>

Administrator

</td><td>

Admin \[admin\]

</td><td>

 

</td><td>

Administrators who can set up unified consumer users.

</td></tr><tr><td>

Internal unified consumer

</td><td>

Internal employee \[snc\_internal\]**Note:** Can have other internal roles across non-CSM applications.

</td><td>

Unified consumer \[sn\_customerservice.unified\_consumer

 **Note:** The unified consumer role doesn't contain snc\_external roles.

</td><td>

An employee \(internal user\) who is also a consumer \(external\).

</td></tr><tr><td>

External unified consumer

</td><td>

 

</td><td>

-   Unified Consumer \[sn\_customerservice.unified\_consumer\]
-   External users \[snc\_external\]

</td><td>

A user who is similar to a consumer \[sn\_customerservice.consumer\], but has the unified consumer role.

</td></tr><tr><td rowspan="3">

Unsupported

</td><td>

Customer Service Management \(CSM\) fulfiller as a consumer

</td><td>

-   Customer service manager \[sn\_customerservice\_manager\]
-   Relationship agent \[sn\_customerservice.relationship\_agent\]
-   Case task agent \[sn\_customerservice.case\_task\_agent\]
-   Account customer agent \[sn\_acct\_consumer.agent\]
-   Location consumer agent \[sn\_customerservice.svc\_location\_consumer\_agent\]
-   Location agent \[sn\_customerservice.svc\_location\_agent\]
-   Location manager \[sn\_customerservice.svc\_location\_manager\]
-   Location relationship manager \[sn\_bus\_loc.location\_relationship\_manager\]
-   Customer service agent \[sn\_customerservice\_agent\]
-   Consumer service agent \[sn\_customerservice.consumer\_agent\]

</td><td>

Unified Consumer \[sn\_customerservice.unified\_consumer\]

</td><td>

A customer service agent who is also a consumer.

</td></tr><tr><td>

CSM contributor as a consumer

</td><td>

-   Account contributor \[sn\_customerservice.account\_contributor\]
-   Consumer contributor \[sn\_customerservice.consumer\_contributor\]
-   Relationship contributor \[sn\_customerservice.relationship\_contributor\]
-   Self-contributor \[sn\_customerservice.self\_contributor​\]
-   Service organization contributor \[sn\_customerservice.service\_organization\_contributor\]
-   Location manager contributor \[sn\_customerservice.svc\_location\_manager\_contributor\]

</td><td>

Unified Consumer \[sn\_customerservice.unified\_consumer\]

</td><td>

An employee \(internal contributor\) who can create cases on behalf of themselves and others, but is also a consumer.

</td></tr><tr><td>

Employee as an account-consumer \(B2B2C\)

</td><td>

Internal employee \[snc\_internal\]

</td><td>

Account consumer \[sn\_acct\_consumer.consumer\]

</td><td>

An employee who is also a consumer for a business-customer \(B2B2C\).

</td></tr></tbody>
</table><table id="table_djy_plq_vzb"><thead><tr><th>

Features

</th></tr></thead><tbody><tr><td>

-   Case Management
-   Case Tasks
-   Install Base Management
-   Inbound/Outbound Email Notifications
-   Targeted Communications
-   Service Catalog Product​ Case
-   Consumer Profile and Consumer Profile Locations
-   Household​
-   Case Application Programming Interface \(APIs\)​​
-   Asset \(IT Asset Management\)
-   Contracts and Entitlements​
-   Contracts on Sold Product or Install Base Items
-   Virtual Agent or​ Agent Chat
-   Live Agent Chat
-   Look up and Verify
-   Case Digest
-   Case Escalations
-   Case Types
-   Case Playbooks for Complaint
-   Case Playbooks for Onboarding
-   Order Management
-   Omnichannel Callback
-   Engagement Messenger
-   ServiceNow Voice for CSM
-   Business Location
-   Walk-up Experience for Customer Service Management
-   Knowledge Management
-   Communities
-   CSM Integrations
    -   Customer Service Management and Field Service Management Integration
    -   Customer Service Management and Request Management Integration
    -   Customer Service Management and Asset Management Integration
-   Field Service Management
    -   Work Orders and Work Order Tasks
    -   Appointment Booking
    -   Conversational Appointment Booking

</td></tr></tbody>
</table>**Related topics**  


[Configuring a user as a Unified Consumer](../concept/configuring-employee-as-a-consumer.md)

[Roles installed with Employee as a Consumer](roles-installed-with-employee-as-consumer.md)

[Setting up a user as a Unified Consumer](../concept/setting-up-a-user.md)

