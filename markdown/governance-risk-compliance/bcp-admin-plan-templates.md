---
title: Configuring plan template
description: As a BCP plan manager, you can create a business continuity plan that can be used for your respective business units during a disruptive event. The Business Continuity Management application provides pre-configured business continuity plan templates. You can streamline the process of a plan creation by using pre-configured plan templates. You can also create a plan template for your business requirement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/bcp-admin-plan-templates.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setup for a BCP, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configuring plan template

As a BCP plan manager, you can create a business continuity plan that can be used for your respective business units during a disruptive event. The Business Continuity Management application provides pre-configured business continuity plan templates. You can streamline the process of a plan creation by using pre-configured plan templates. You can also create a plan template for your business requirement.

You can view the pre-configured plan templates for business continuity planning in the **General Administration** section in the application navigator.

Using a plan template gives you a standard plan layout that has the document sections, loss scenarios, and primary elements that are to be recovered. Plan templates help you to focus on the plan content, its tasks, and the effective implementation of the plan.

Creating a plan helps an organization to identify processes, locations, and assets that must be recovered as a priority when there is a disruption. Selecting a plan type helps to identify the elements for recovery and the time by which it should be done.

## Using business continuity plan templates

The Business Continuity Management application provides these business continuity plan templates that are installed with demo data:

-   **Application DR Plan**
-   **Business Continuity Plan**
-   **Datacenter Recovery Plan**
-   **Workplace Recovery Plan**

The business continuity plan templates that are installed with demo data are shown in the example.

\[Omitted image "bcm-plan-templates.png"\] Alt text: Demo data.

See the table for more information on different types of demo data plan templates that you can use in the Business Continuity Management application.

|Name|Primary element recovered|Description|
|----|-------------------------|-----------|
|Application DR Plan|Applications|Plan to recover an IT application following a disruptive event. A sample Application DR Plan template is shown in the example.\[Omitted image "application-dr-plan-template.png"\] Alt text: Application DR Plan template.|
|Business Continuity Plan|Business Processes|Plan to continue operations of a core business process or processes during a disruption to workplaces, applications, or critical vendors. A sample Business Continuity Plan template is shown in the example. \[Omitted image "business-continuity-plan-template.png"\] Alt text: Business Continuity Plan template.|
|Datacenter Recovery Plan|Datacenters|Plan to recover a datacenter following a natural disaster or significant event that impacts the availability of a datacenter. A sample Datacenter Recovery Plan template is shown in the example.\[Omitted image "datacenter-recovery-plan-template.png"\] Alt text: Datacenter Recovery Plan template.|
|Workplace Recovery Plan|Locations|Plan to recover a workplace in the event that one of them becomes unusable or uninhabitable. A sample Workplace Recovery Plan template is shown in the example.\[Omitted image "workplace-recovery-plan-template.png"\] Alt text: Workplace Recovery Plan template.|

## Creating a plan template for your business requirement

Instead of using the demo data templates, you can create a template for your specific requirement. For more information on creating a plan template for your business requirement, see [Configure the business continuity plan template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-a-bcp-template-uib-ws.md).

## Pre-populating tasks and strategies with templates

Plan templates can reference recovery strategy templates, task template groups, and task templates. When a planner creates a plan from such a template, the system creates the corresponding records automatically:

-   Plan-level task template groups and task templates produce tasks on the plan **Recovery tasks** tab.
-   Loss-scenario-level templates produce tasks on the loss scenario **Recovery tasks** tab.
-   Recovery-strategy-level templates produce tasks on the recovery strategy **Recovery tasks** tab.

Task dependencies that are defined inside a task template group are preserved on the created tasks.

-   **[Configure the business continuity plan template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-a-bcp-template-uib-ws.md)**  
Configure the business continuity plan template in the Business Continuity Management application for your business. You can use the plan template to recover a specific primary element such as Employees or Web Servers. Similarly, you can create a plan template for different plan authoring types such as documentation, loss scenarios, and recovery tasks.
-   **[Configure Task templates and Task template groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-task-temp-temp-groups.md)**  
Create task templates and task template groups to save individual tasks or groups of tasks for reuse. Add templates to new plans or insert them into existing ones.

**Parent Topic:**[Setup for a business continuity plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-admin-tasks.md)

