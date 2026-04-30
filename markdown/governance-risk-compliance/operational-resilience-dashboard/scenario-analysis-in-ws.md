---
title: Conducting a scenario analysis
description: By performing a scenario analysis, you can determine the risks that might impact your business. You can analyze the impact of the scenarios and events on your business services. You can also track the actions and improvements from the scenario analysis in Operational Resilience Workspace.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Conducting a scenario analysis

By performing a scenario analysis, you can determine the risks that might impact your business. You can analyze the impact of the scenarios and events on your business services. You can also track the actions and improvements from the scenario analysis in Operational Resilience Workspace.

## Overview of a scenario analysis

Scenarios represent the business-specific risks that are used to test how events can impact your organization. By performing a scenario analysis, you can analyze the impact of the scenarios and their associated events on your business services. Each service has a few dependencies associated with it. The **Compute Operational Resilience Compliance** scheduled job runs in the background and populates the dependencies for the services. As an owner of the scenario analysis, you can request a plan approval.

When a plan approver approves the plan approval, it triggers a response task for the scenario analysis. Participants of the analysis work on the response tasks and add their observations on the analysis.

As an owner of the scenario analysis, you can verify the status of the services and calculate the possible disruptions. After the response tasks have been completed, you can request an analysis approval for your scenario analysis. When an analysis approver approves the scenario analysis, you can close it and monitor its status in Operational Resilience Workspace.

## Tasks to set up a scenario analysis

If you've got the sn\_oper\_res.manager role, you can set up a scenario analysis as follows:

1.  Create a scenario that helps you to determine the risks that are applicable to your business.
2.  Assign an owner, a plan approver, and an analysis approver to the scenario analysis in the scenario analysis form.
3.  Add the scope and dependencies that are applicable to your scenario.
4.  Associate one or more scenario events with the scenario analysis. Add the participants, services, dependencies, and issues that are specific to a scenario event. When a scenario event is associated with a participant, a response task is automatically generated on the **Responses** tab and it’s assigned to the participants.
5.  Send the scenario analysis to the plan approver of the scenario analysis and request for a plan approval.
6.  Collect the observations, gaps, and recommendations from the participants about the scenario analysis event. The participants of a scenario event are the users with at least the sn\_oper\_res.user roles from the associated business functions, such as Finance or HR departments.
7.  Compare the impact tolerance with the disruption duration to determine if any service was breached.
8.  Close the open response tasks and open scenario events that are associated with your scenario analysis.
9.  Send the scenario analysis to the analysis approver for a review and request an approval for the scenario analysis.
10. Close the scenario analysis and monitor its status in Operational Resilience Workspace.

## States and UI actions that are associated with a scenario analysis

The states and UI actions that are associated with a scenario analysis are described in the following table.

<table id="table_amh_4kb_cv"><thead><tr><th>

State

</th><th>

UI action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

In the All scenario analysis form, select **New**.

</td><td>

More details about the UI actions for this state:

-   In the All scenario analysis form, select **New**, add information in the **Details** tab, and select **Save**. A record is automatically created in the **Draft** state.
-   On the **Scope** tab, select **Add** to add a service from the list of the available services.

**Note:** The services are fetched from the Services \(OR\) entity type in the Operational Resilience application.

-   Some services in the Operational Resilience application are associated with specific dependencies, for example, Acer or Adtran. To select a service that is associated with a dependency, select **Add dependency related scope**.

-   On the **Dependencies** tab, select **Add** to associate a dependency with the scenario analysis as shown in the following example. Some dependencies are associated with specific services. You can add a dependency that is related to a specific service by selecting **Add scope related dependency**.

-   To save the selections, select **Save**.

-   In the scenario analysis form, select **Request plan approval** to request a plan approval from the plan approver of the scenario analysis.

**Note:** You must associate at least one service to begin the scenario analysis.​


</td></tr><tr><td>

Pending plan approval

</td><td>

Navigate to the **Approvals** tab, update the state from **Requested** to **Approved,** and then in scenario analysis form, select **Save**.

</td><td>

More details about the UI actions for this state:

-   As the plan approver of the analysis, you must review the scope of the analysis in the **Pending plan approval** state. You can check the setup of the associated services, participants, scenario events, and issues.
-   To approve the plan for the analysis, navigate to the **Approvals** tab, update the state from **Requested** to **Approved**, and then in the scenario analysis form, select **Save**.
-   When you approve the plan for the scenario analysis and save it, the state of the scenario analysis is updated to **Analyze**.

-   If you reject the plan, the state of the scenario analysis is reset to **Draft**.

</td></tr><tr><td>

Analyze

</td><td>

On the **Scenario events** tab, add a scenario event to the analysis by selecting **Add**. On the **Participants** tab, add a participant to the analysis by selecting **Add**.

 On the **Scenario events** tab, update the state to **Closed** to close the scenario event. Select **Request analysis approval**.

</td><td>

More details about the UI actions for this state:

-   In this state, the participants of the scenario analysis can add their work notes in the scenario analysis form and work on events that are based on their responsibility.

**Note:** You must add at least one service, one participant, and one scenario event before proceeding with the scenario analysis.​

-   On the **Scenario events** tab, select **Add** to associate one or more scenario events with the analysis.

-   On the **Participants** tab, select **Add** to associate one or more participants with the analysis. When a scenario event is created, a response task is automatically created and assigned to the participant. You can collect the feedback from the participants and review their observations, gaps, and recommendations for each associated event on the form.

-   Navigate to the **Responses** tab and close the response tasks that are associated with a scenario event.

-   Update the state of the scenario event from **Draft** to **Completed** and close the open scenario event. Select **Save**.

-   Based on the observations and recommendations, the details of the scenario analysis are auto-filled in this state in the scenario analysis form. To request an approval from the analysis approver, in the analysis form, select **Request analysis approval**. The state of the scenario analysis is then updated to **Pending analysis approval**.


</td></tr><tr><td>

Pending analysis approval

</td><td>

Navigate to the **Approvals** tab and update the state from **Requested** to **Approved**.

</td><td>

If you're the analysis approver, you can review the analysis scope in this state. Check the progress on the analysis for the selected business service. You can then approve or reject the analysis.

</td></tr><tr><td>

Approved

</td><td>

In the analysis form, select **Save**.

</td><td>

When you approve the scenario analysis, the state of the scenario analysis is updated to **Approved**. If you reject the scenario analysis, the state of the scenario analysis is reset to **Analyze**.

 When the state of the scenario analysis is in the **Approved** state, you can close the scenario analysis.

</td></tr><tr><td>

Closed

</td><td>

In the analysis form, select **Close**.

</td><td>

As an owner of the scenario analysis, you can close the scenario analysis. The state is updated to **Closed**.

</td></tr></tbody>
</table>## Fetching the service entities from the Services \(OR\) entity type

The Operational Resilience application fetches the service entities from the Services \(OR\) entity type as shown in the following example.

![Services OR entity type.](../image/entity-type-module-view-in-list-4.png "Services OR entity type")

Users with the sn\_oper\_res.admin role can view the Entity Types module and its related lists in the Operational Resilience application UI as shown in the following example.

![Service entities under the Services OR entity type.](../image/entities-under-services-or-entity-type-5.png "Service entities under the Services OR entity type")

**Note:** You can only select the entities that belong to the Facilities, People, Suppliers, and Technology pillars. The Services and Processes pillars are filtered out from the list of the pillars for the entities.

## Dependencies for the services

Each service has a few dependencies associated with it. The **Compute Operational Resilience Compliance** scheduled job runs in the background and populates the dependencies for the services. The following example shows that the Addison, TX United States HVAC entity is listed as a dependency for supporting the Faster Retail Payments service.

![Dependencies for the services.](../image/dependencies.png "Dependencies for the services")

You can only select the dependencies that belong to the Facilities, People, Suppliers, and Technology pillars. The Services and Processes pillars are filtered out from the list of the pillars for the dependencies.

## Response tasks

As a scenario analysis owner, when you create a scenario event and add a participant to it, a response task is automatically created for the participant. When a participant is assigned to a scenario event, a response task is created. An email notification is automatically sent to the participant.

On the **Responses** tab, the details of the response task such as the response task number, name of the assigned participant, and state of the response task are displayed.

The owner of the scenario event can add a service and a dependency to the response task. The assignee of the response task can complete the response task, add their notes about the scenario event, and update the impact duration of the scenario event as shown in the following example.

![Notes about the scenario event.](../image/sce-event-notes.png "Notes about the scenario event")

## Known issue for upgrading from Release 15.x.x to Release 16.x.x

While upgrading from Release 15.x.x to Release 16.x.x, if you have a scenario analysis in the **Analyze** state and a participant is already added to the scenario analysis, a response task is not created automatically. This is a known issue.

As a workaround for this issue, the Operational Resilience manager must remove the participants from the scenario analysis and add them to the same scenario analysis. The Operational Resilience application then automatically creates a response task for the scenario analysis.

**Note:** You can also choose to proceed with the scenario analysis without a response task.

## Summary of the services, scenarios, disruptions, and events

You can view information on the services, scenarios, disruptions, and events in the Summary panel as shown in the following example.

![Summary panel of the scenario analysis form.](../image/summary-panel.png "Summary panel of the scenario analysis form")

The Summary panel provides information about the business services, associated scenarios, disruptions, and events. For a description of the field values, see the following table.

|Field|Description|
|-----|-----------|
|Number of services|Number of services that are associated with the scenario analysis.|
|Number of services under impact tolerance|Number of services that are associated with the scenario analysis and that are under the impact tolerance.|
|Number of services above impact tolerance|Number of services that are associated with the scenario analysis and that are above the impact tolerance.|
|Number of scenarios|Number of scenarios that are associated with the analysis.|
|Number of scenarios completed|Number of completed scenarios that are associated with the analysis.|
|Number of events|Number of events that are associated with the analysis.|
|Number of events completed|Number of completed events that are associated with the analysis.|
|Disruption duration|Time duration between the end time of the last event and the start time of the first event. It is displayed in the number of days.|
|Duration of events with overlaps|Summary of all event durations including the overlapping events and pauses. It is displayed in the number of days and minutes.|
|Duration of events without overlaps|Summary of all event durations without the overlapping events and pauses. It is displayed in the number of days and minutes.|

