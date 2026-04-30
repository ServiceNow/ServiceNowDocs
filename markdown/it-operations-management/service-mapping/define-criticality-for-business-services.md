---
title: Define criticality for application services
description: For each service instance, select a criticality level that reflects how important it is to your organization operations.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Application service completion, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Define criticality for application services

For each service instance, select a criticality level that reflects how important it is to your organization operations.

## Before you begin

Determine how important the application service is to your organization.

Role required: service\_mapping\_admin

## About this task

Typically, you might assign high criticality to service instances, which impact your customer base or sales revenue, while giving low criticality to internal service instances causing minor inconvenience to organization employees. For example, you could set high criticality for a service instance that supports sales functionality using the organization web site. A service instance that provides internal printing for the organization employees could receive low criticality.

You can also use a criticality value to define recovery strategies.

![Criticality levels as displayed on the Operator Workspace page](../../service-operations-workspace-itom/image/Operator-Workspace-Page.png "Criticality levels displayed in Operator Workspace page")

## Procedure

1.  In the classic environment, perform the following steps:

    1.  Navigate to **All** &gt; **Service Mapping** &gt; **Home**.

        The Home page displays only information on service instances that Service Mapping can discover or already discovered. The Home page does not display information on service instances that are created manually or using the API.

    2.  Click **View Your Services** on the **Completed** tile.

    3.  Select the relevant application service.

    4.  Click **Additional Info**.

    5.  Select the appropriate option from the **Business criticality** list.

    6.  Click **Update**.

2.  Alternatively, perform the following steps in the Agent Workspace UI:

    1.  Navigate to **Agent Workspace** &gt; **Agent Workspace Home**.

    2.  Click **Lists** in the left pane.

    3.  Navigate to **Services** &gt; **All Services**.

        The list of services displays services in Operational status.

    4.  Select the relevant application service.

    5.  Click the **Open Preview** icon.

        ![Open Preview icon next to the selected application service.](../image/workspace-all-services-open-preview.png)

        The Details pane opens on the right.

    6.  Select the appropriate option from the **Business criticality** list.

    7.  Click **Update**.


**Parent Topic:**[Application service completion](../concept/advanced-business-service-definitions.md)

**Related topics**  


[Group application services](organizing_services-into-groups.md)

[Control user access to application services](control-user-access-to-business-services.md)

[Schedule a top-down discovery by Service Mapping](t_CreateDiscoSchedForCITypes.md)

[Service definition transfer from one instance to another](../concept/transfer-service-definitions.md#)

