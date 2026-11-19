---
title: Configuring Field Service Management using Guided Setup
description: The Field Service Management Guided Setup provides a sequence of tasks that help you import and configure the foundation data for Field Service Management on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/field-service-management/configuring-fsm-with-guided-setup.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Plan implementation, Configure, Field Service Management]
---

# Configuring Field Service Management using Guided Setup

The Field Service Management Guided Setup provides a sequence of tasks that help you import and configure the foundation data for Field Service Management on your ServiceNow instance.

## Before you begin

Role required: wm\_admin

Some tasks need an additional role, for example user\_admin to create users and groups, or sn\_cmdb\_admin to define model categories. If you don't have the role, the task can't be completed from guided setup. For the role that each task needs, see [Roles required for Field Service Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/roles-required-for-field-service-guided-setup.md).

The advantages of using guided setup for Field Service Management are:

-   A single interface gives you access to the configuration tasks for the whole product, so you don't search the navigation for each module.
-   Configuration tasks are grouped into categories, each with a description, a task count, and a status.
-   The percentage complete for each category and for the whole setup shows what is left to do.

## About this task

Guided setup covers the basic configuration only. It doesn't include every feature and capability of Field Service Management.

Each category appears as a card on the **Welcome to Field Service Guided Setup** page. The card shows the percentage complete, the status \(for example **Not Started**\), the number of tasks completed, and the list of tasks in the category.

**Note:** This guided setup assists you with only the basic configuration and doesn’t include all the features and capabilities of Field Service Management.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Guided Setup**.

2.  On the **Welcome to Field Service Guided Setup** page, review your overall progress and the status of each category.

    -   The overall percentage complete appears at the top of the progress tracker on the left.
    -   Use the **Filter** list to change which categories appear. The default is **Show all**.
3.  Select **Get Started** on the category that you want to configure.

    Complete the categories in the order shown, because later categories build on earlier ones. For example, create users and groups in **Foundation Data** before you assign scheduling and dispatch in **Field Service Process**.

    The tasks in the category appear.

4.  Select **Configure** on a task to begin it.

    Each task opens the page where you perform the configuration. For descriptions of what each task configures, see the table that follows these steps.

5.  Select **Mark as Complete** after you finish a task.

6.  Repeat steps 3 to 5 for each task and each category that applies to your organization.

<table id="table_fsm_gs_categories"><thead><tr><th>

Category

</th><th>

What you configure

</th><th>

Tasks \(role required\)

</th></tr></thead><tbody><tr><td>

Foundation Data

</td><td>

Locations, users, and groups that provide role-based access to the instance and support automated processes such as dynamic scheduling. Assign roles to groups or to individual users, and assign skills and location coverage to groups to determine task routing.

</td><td>

-   Define Locations \(import\_admin\)
-   Create Users \(user\_admin\)
-   Create Groups \(user\_admin\)
-   Assign Group Roles \(user\_admin\)


</td></tr><tr><td>

Products, Assets, and Inventory

</td><td>

Product models, which are the basis for assets. Assets can be in use at a customer or internal site, or in stock in a stockroom. Field Service Management checks current inventory to make sure parts are available and tasks are assigned appropriately.

</td><td>

-   Define Model Categories \(sn\_cmdb\_admin\)
-   Create Product Models \(sn\_cmdb\_admin\)
-   Create Stockrooms \(wm\_admin\)
-   Create Stock Rules \(wm\_admin\)
-   Create Assets \(wm\_admin\)


</td></tr><tr><td>

Field Service Process

</td><td>

How work orders and tasks are created, qualified, and dispatched, how parts are sourced, and how technician routes and schedules are created.

</td><td>

-   Configure Field Service Management \(wm\_admin\)
-   Work Order Templates \(wm\_admin\)
-   Scheduling and Dispatch \(wm\_admin\)
-   Define SLAs \(wm\_admin\)
-   Self-Service Appointment Booking \(wm\_admin\)


</td></tr><tr><td>

Field Service Workflow

</td><td>

The lifecycle of work orders and work order tasks from creation to closure, which the **State** field tracks. UI actions on the work order and work order task forms trigger the transitions between states.

</td><td>

-   State Flows \(wm\_admin\)
-   UI Actions \(ui\_action\_admin\)
-   Questionnaires \(wm\_admin\). For more information, see [Field Service Management questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/field-service-management-questionnaires.md).
-   Time Recording \(wm\_admin\). For more information, see [Time Recording for Field Service components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/components-time-recording-fsm.md).
-   Contextual Search \(wm\_admin\)


</td></tr><tr><td>

Mobile

</td><td>

The mobile application lets technicians use an Android or iOS device to accept or reject tasks, track travel and work time, get driving directions, and check schedules. Technicians can also scan bar codes to identify parts and collect task details with questionnaires. Customers can acknowledge completed work with a signature on the mobile device.

</td><td>

Configure Mobile Application

</td></tr><tr><td>

Planned Maintenance

</td><td>

Regular preventive maintenance of assets. Maintenance plans and schedules trigger the creation of work orders or facilities requests that specify the asset and the type of maintenance to perform. The Planned Maintenance application works with Field Service Management.

</td><td>

-   Create Maintenance Plans \(wm\_admin\)
-   Create Maintenance Schedules \(wm\_admin\)


</td></tr><tr><td>

Google Maps

</td><td>

Mapping, routing, and geolocation capabilities, which a Google Maps API key in your instance significantly enhances. A Google Maps API Premium Plan is typically required to fully use the capabilities of Field Service Management.

</td><td>

-   Input Google Maps API Key \(wm\_admin\)
-   Enable Google Maps API Travel Time \(wm\_admin\)


</td></tr><tr><td>

Contractor Management

</td><td>

Onboarding of contractor companies and their external workforces, such as managers and field agents. Field service administrators and internal contractor managers can set up groups to route work order tasks to contractor companies. This category is locked until you activate the required plugins.

</td><td>

-   Onboard Contractor Company \(admin\)
-   Onboard External Manager \(user\_admin\)
-   Create Group \(user\_admin\)
-   Configure Group selection criteria \(user\_admin\)
-   Onboard External Agent \(user\_admin\)


</td></tr></tbody>
</table>
## Result

Guided setup updates the percentage complete and the status of each category as you complete tasks. When every category that applies to your organization is complete, the basic configuration of Field Service Management is done.

**Related topics**  


[Roles required for Field Service Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/roles-required-for-field-service-guided-setup.md)

[Planning your Field Service Management implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/planning-implementation-fsm.md)

