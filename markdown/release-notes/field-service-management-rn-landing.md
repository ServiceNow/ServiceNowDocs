---
title: Field Service Management release notes
description: Field Service Management has new and updated features in the Brazil releaseThe ServiceNow Field Service Management \(FSM\) application enables your organization to efficiently manage Field Service operations including work order dispatch, scheduling, and mobile workforce enablement. Field Service Management was enhanced and updated in the Brazil release.Field Service Management enhancements and new features in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/field-service-management-rn-landing.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Field Service Management release notes

Field Service Management has new and updated features in the Brazil release

**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/new-features-changes.md)

## Field Service Management release notes

The ServiceNow® Field Service Management \(FSM\) application enables your organization to efficiently manage Field Service operations including work order dispatch, scheduling, and mobile workforce enablement. Field Service Management was enhanced and updated in the Brazil release.

### About Field Service Management

-   Create, dispatch, and track work orders across your field service operations.
-   Manage technician and contractor capacity, skills, and availability to optimize resource allocation.
-   Track inventory, assets, and planned work to confirm crews have what they need in the field.
-   Monitor field service performance, quality metrics, territory planning, crew operations, and contractor work to meet customer commitments and service level agreements.
-   Use ServiceNow Otto AI capabilities to help technicians, dispatchers, and managers work more efficiently and close tasks faster.

See [Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/fsm-application-landing-page.md) for more information.

### Activation and other requirements

**Note:** Field Service Management is available in the ServiceNow Store. For details, see .

-   **Activation information**

    Install Field Service Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


## 2026 September Monthly

Field Service Management enhancements and new features in the Brazil release.

### What's new

-   **[Schedule Optimization v1.2 support for overlapping territories during prioritized optimization](https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-schedule-optimization.html)**

    Expand prioritized event optimization to include overlapping territories when determining the technicians and tasks directly impacted by an event. Configure a search radius at the qualifier level to control which overlapping territories are considered.

-   **[Schedule Optimization v1.2 supports matching rules with four additional matching dimensions for prioritized event optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/triggering-optimization-on-task-or-agent-availability-change.md)**

    Matching rules for prioritized event optimization now support four additional matching dimensions that enable you to filter technicians and tasks based on specific criteria:

    -   retrieve tasks based on skills
    -   retrieve technicians based on skills
    -   retrieve tasks within radius
    -   retrieve technicians within radius
    Combine matching dimensions using AND logic \(all must match\) and OR logic \(any can match\) to more precisely identify which technicians and tasks are directly impacted by events. Configure matching dimensions at the qualifier level to define which technicians and tasks are considered for assignment.

-   **[Schedule Optimization v2.0 skill level and skill expiration support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/skills-table-fields.md)**

    Control how skill requirements are evaluated during Schedule Optimization. Define whether a task requires a specific skill level or any level of a skill, and configure start and end dates for technician skills. Schedule Optimization assigns only technicians with valid qualifications.

-   **[Schedule Optimization v 2.0 expanded Run Summary details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/monitoring-schedule-optimization-runs.md)**

    Gain more visibility into Schedule Optimization results. The Run Summary now displays the optimization horizon, including the start and end dates of the optimization window, and shows all shifts considered during optimization with status and reason codes. Review job-level and qualifier-level optimization metrics and shift plans with their assigned tasks.

-   **[Schedule Optimization v2.0 support time-bound availability of demand channel in a territory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/hard-soft-constraints.md)**

    Assign tasks only to eligible technicians based on the demand channel mapping and availability. For example, a technician mapped to Installation demand channel on Mondays is assigned only Installation tasks scheduled on Mondays.

-   **[Dispatcher Workspace v11.0 view breaks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/view-task-calendar.md)**

    View break and lunch details directly within task events on the calendar in Dispatcher Workspace. Dispatchers no longer need to open a separate record to see when an agent is on break. Lunch breaks can be viewed directly within scheduled tasks.

-   **[Proxy Actions v1.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/configure-proxy-fsm.md)**

    Proxy Actions let an agent or manager perform specific actions on a work order task on behalf of another technician — someone other than the person the task is actually assigned to. Proxy action policies are administered through a dedicated policy form. The Proxy Admin role automatically inherits delegation admin permissions.

-   **[Manager Workforce v2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/using-team-calendar.md)**

    Embedded lunch breaks are now visible and editable directly within Workforce, with break status icons updating automatically as break state changes. Technicians and managers can track and manage break status changes. Lunch breaks can now be embedded directly within scheduled tasks rather than tracked as separate events.

-   **[Scheduling AI Agent Collections v2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/now-assist-shift-manage.md)**

    ServiceNow Otto for FSM can now update and delete shifts and schedules on request.

-   **[Shift Scheduling v8.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/embedded-breaks-and-lunches.md)**

    Embed breaks and lunches directly within a work order task. Breaks can transition automatically at their scheduled start and end time, or require manual action from the technician, based on the new Auto-status breaks setting. Either way, the work order task pauses and resumes with the break, with the change logged to the work notes in a work order task.

-   **[FSM Configurable Dispatcher Workspace Bundle v11.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/quick-filters-dw.md)**

    Dispatchers can build quick filters for the task panel and calendar using criteria such as skill, parts, and SLA breach. A task filter removes tasks that don't match, while a calendar filter grays them out instead of removing them.


### What's changed

-   **Schedule Optimization**

    The Run Summary "Technicians" tab is renamed to "Dropped Technicians".


### What's deprecated or removed

-   **Schedule Optimization custom queue properties removed in v2.0**

    Starting with the Brazil release, the following Schedule Optimizationcustom queue properties are no longer deployed, enhanced, or supported:

    -   sn\_schedule\_optim.data\_processor\_number\_of\_queues
    -   sn\_schedule\_optim.solution\_processor\_number\_of\_queues
    -   Claim limit properties for all data queues \(1–8\) and all event queues \(1–8\)
    -   Event distribution properties for all data queues \(1–8\) and all event queues \(1–8\)
    These properties have been replaced by Queue Registries. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


### Plugin information

-   **New plugins**

    Proxy Actions for Field Service Management \(sn\_fsm\_proxy\_actn\): Allows for the configuration of proxy actions. Proxy Actions let a technician or manager perform specific actions on a work order task on behalf of another technician.

-   **Plugins planned for deprecation**

    [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home)

    The following plugins are planned for deprecation in the D release. Beginning with the Brazil release these plugins will be migrated to a store application. Upgrade your instance to Brazil or later release versions and the store applications will be automatically installed.

    Beginning with the Brazil release, the following applications have been moved to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Any application enhancements will be delivered through the related store app.

    -   Appointment Booking \(com.snc.appointment\_booking\)
    -   Dynamic Scheduling \(com.snc.dynamic\_scheduling\)
    -   Field Service Crew Operations \(com.snc.fsm\_crew\_scheduling\)
    -   Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\)
    -   Field Service Management \(com.snc.work\_management\)
    -   Field Service Management Access Hours Management \(com.snc.fsm\_access\_hours\)
    -   Field Service Multi-Day Task Scheduling \(com.snc.fsm\_multiday\_tasks\)
    -   Field Service - Questionnaire \(com.snc.wm\_questionnaire\)
    -   Field Service Task Bundling \(com.snc.fsm\_task\_bundle\)
    -   Field Service Task Dependency \(com.snc.fsm\_task\_dependency\)
    -   Field Service Work Configurations \(com.snc.fsm\_work\_types\)
    -   Resource Scheduling \(com.snc.fsm\_resource\_scheduling\)
    -   Service management geolocation \(com.snc.geolocation\)
    -   Task Grouping \(com.snc\_task\_grouping\)

