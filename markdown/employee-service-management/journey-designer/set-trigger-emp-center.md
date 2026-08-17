---
title: Set Onboarding ramp up trigger to use Employee Center portal
description: Set Onboarding ramp-up trigger to use Employee Center portal in the trigger configuration so the onboarding ramp-up plan workflow is accessible through the portal. Without setting the portal, the trigger will not be visible or usable in the Employee Center portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/journey-designer/set-trigger-emp-center.html
release: australia
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generate onboarding ramp-up plan, AI in Journey designer, Use, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Set Onboarding ramp up trigger to use Employee Center portal

Set Onboarding ramp-up trigger to use Employee Center portal in the trigger configuration so the onboarding ramp-up plan workflow is accessible through the portal. Without setting the portal, the trigger will not be visible or usable in the Employee Center portal.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the **All** menu, and enter `sn_aia_trigger_configuration.list` in the navigation filter.

    The AIA Trigger Configuration \[sn\_aia\_trigger\_configuration\] table appears.

2.  Select **Onboarding ramp-up trigger** from the list of AI agent triggers.

3.  Add the **Active** and **Portal** fields to the form if they aren’t available.

    1.  Select and hold \(or right-click\) the form header and select **Configure** &gt; **Form layout**.

    2.  Select **Active** and **Portal** from the Available list, and then select the **Add** icon to move the fields to the Selected list.

    3.  Select **Save**.

4.  Select the **Active** check box.

5.  Set the **Portal** field to **Employee Center**.

6.  Select **Update**.


**Parent Topic:**[Generate onboarding ramp-up plan agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/onboarding-ramp-up-plan-agentic-wf.md)

