---
title: Automating seat assignment for new hires
description: Use HR Service Delivery and Workplace Service Delivery to automatically assign a seat for the new hires in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/auto-assign-new-hires.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Automating seat assignment for new hires

Use HR Service Delivery and Workplace Service Delivery to automatically assign a seat for the new hires in your organization.

The automated seat assignment feature integrates Workplace Case Management and Journey designer to connect HR onboarding activities with workplace assignment. The pre-boarding activity in the onboarding lifecycle event contains an activity to automatically assign a workspace \(seat or neighborhood\) to new employees.

## Configuration overview

To use the automated seat assignment feature, you must install plugins in the following order. You must have the System Administrator \(admin\) role to install plugins.

1.  Install the Journey designer plugin along with its demo data.

    For more information about installing Journey designer, see [Installation and configuration overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/jny-inst-config-overview.md).

2.  Install the Workplace Space Management plugin along with its demo data.

    For more information about installing Workplace Space Management, see [Install Workplace Space Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-space-management/install-workplace-space-mgmt.md).

3.  Configure a value for the **sn\_wsd\_core.ALLOCATION\_TYPE** property.

    The system analyzes and assigns spaces based on the property value. For example, if the property is set to Cost Center, the system looks for a space with the same Cost Center as the new employee's manager.

    **Note:** This step is not required for neighborhood assignments.

4.  Install the Workplace Case Management plugin.

    For more information about installing Workplace Case Management, see [Install Workplace Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/install-workplace-case-mgmt.md).


**Note:** If you have earlier versions of the plugins installed, update the Journey designer plugin and reinstall the demo data. Then update the Workplace Space Management plugin and reinstall the demo data.

## Process overview

1.  An HR manager or journey owner initiates an onboarding journey for a new employee. For more information about creating a journey, see [Create a journey](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/jny-dsgnr-create-journey.md).
2.  The hiring manager fills in basic information about the employee. For more information about journey view for a manager, see [Journey view for a manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/manager-journeys-view.md).
3.  When the pre-boarding lifecycle event starts, the system creates a workplace case with the service `Workplace Location Assignment`. For more information about the Workplace Location Assignment service, see [Workplace Location Assignment service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/location-assignment-service.md).

    The employee and their manager can view the status of the workplace case from the Journeys page on the Employee Center.

    **Note:** To view workplace cases for employees, the manager must have the `sn_wsd_core.workplace_user` role.

4.  The system analyzes the locations of the employee's team and assigns a location or neighborhood to the employee's profile.

    For neighborhood assignments, if the user qualifies for a neighborhood, the system closes the workplace case with a work note. the `Assign Users to Neighborhood` scheduled job assigns the profile to the neighborhood.

    For location assignments, the system follows the configured workplace service.

    If the system can't find a space or neighborhood for the employee, a manual assignment task is created. A case manager or agent can then assign a location to the employee.

5.  After the space is assigned to the profile, the system sends an email to the employee and their manager with the location details.

**Parent Topic:**[Configuring Workplace Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management]()

[Create a Workplace case template]()

[Create a Workplace task template]()

[Smart Assessment for Workplace Case and Task]()

[Configure Approval options]()

[Configure a Record producer]()

[Configuring a record producer for request edit]()

[Configuring a record producer for reservation]()

[Create an SLA Definition]()

[Create a Workplace service]()

[Add a workplace service item to a workplace service]()

[Create a workplace template configuration]()

[Create a workplace field mapping]()

[Configure an escalation rule]()

[Add Fulfillment instructions]()

[Group similar workplace cases under a parent case]()

