---
title: Using Customer Service Management with Safe Workplace applications
description: Screen consumers and contacts for compliance with health and safety policies to determine whether they are permitted to enter a location.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating with Safe Workplace applications, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Using Customer Service Management with Safe Workplace applications

Screen consumers and contacts for compliance with health and safety policies to determine whether they are permitted to enter a location.

To ensure that consumers and contacts can enter a location safely after emergencies and pandemics, consumers or contacts fill out a Health Verification form and health screeners or customer or consumer service agents perform a health screening.

**Note:** Typically, you receive an email or a mobile notification with a link to the health verification form. Alternatively, you can search for the health verification form on the Consumer or Customer Service Portal.

## Roles required

Users with the roles listed in the following table can use Customer Service Management with Safe Workplace applications.

<table id="table_w1d_534_ymb"><thead><tr><th>

Role

</th><th>

Task

</th></tr></thead><tbody><tr><td>

sn\_customerservice.consumer or sn\_customerservice\_customer

</td><td>

Access and complete the Health Verification form on the Consumer or Customer Service Portals. **Note:** For more information on filling out the form, see [Verify your health status and compliance](https://www.servicenow.com/docs/access?context=agree-compliance-return&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

</td></tr><tr><td>

sn\_imt\_monitoring.monitoring \_user

</td><td>

Screen external users entering a location to ensure compliance with entry requirements. **Note:** Health screeners cannot view additional Customer Service Management information on the screening form.

For more information on screening, see [Conduct a health screen for entry](https://www.servicenow.com/docs/access?context=screen-returning-employee&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

</td></tr><tr><td>

sn\_customerserviceagent with the sn\_imt\_monitoring.monitoring\_user role

</td><td>

Screen contacts entering a location to ensure compliance with entry requirements. The **Accounts** field for contacts is displayed by default on the screening form. Other fields that have been configured for contacts are also visible.

</td></tr><tr><td>

sn\_customerservice.consumer\_agent with the sn\_imt\_monitoring.monitoring\_user role

</td><td>

Screen consumers entering a location to ensure compliance with entry requirements. The **Suffix** field for consumers is displayed by default on the screening form. Other fields that have been configured for consumers are also visible.

</td></tr></tbody>
</table>