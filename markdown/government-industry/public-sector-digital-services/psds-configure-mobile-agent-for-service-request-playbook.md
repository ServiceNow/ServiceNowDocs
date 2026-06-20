---
title: Configure Mobile Agent for Service Request Playbook
description: Install the Customer Service Mobile and Service Request Playbook plugins to enable government service agents to track non-emergency service requests on the Mobile Agent. You can then configure the roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/government-industry/public-sector-digital-services/psds-configure-mobile-agent-for-service-request-playbook.html
release: xanadu
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Request Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure Mobile Agent for Service Request Playbook

Install the Customer Service Mobile and Service Request Playbook plugins to enable government service agents to track non-emergency service requests on the Mobile Agent. You can then configure the roles.

As a user with the admin role, complete the following configuration tasks to set up the Mobile Agent application.

<table id="table_cmk_mdm_fwb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Install Service Request Playbook application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/government-industry/public-sector-digital-services/install-psds-service-request-playbook.md)

</td><td>

Install Service Request Playbook \(sn\_gsm\) from the ServiceNow® Store.

</td></tr><tr><td>

Activate the Customer Service Mobile plugin \(com.sn\_csm\_mobile\)

</td><td>

You can activate the Customer Service Mobile plugin \(com.sn\_csm\_mobile\) using the Customer Service Management guided setup.

</td></tr><tr><td>

\(Optional\)  plugin \(com.snc.work\_management\)

</td><td>

Install the Field Service Management plugin to view the work orders related list. For more information, see [Integration with Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/government-industry/public-sector-digital-services/psds-integration-fsm.md).

</td></tr><tr><td>

[Configure public sector roles and permissions for Mobile Agent app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/government-industry/public-sector-digital-services/psds-mobile-app-configure-roles-admin.md)

</td><td>

Configure user roles in order for government service agents to access the Mobile Agent app. This step is mandatory for any government service agent to be able to work from the app.

</td></tr></tbody>
</table>Once the Customer Service Management mobile application is activated and configured, agents can download the ServiceNow Mobile Agent on their mobile devices and access ServiceNow instances.

