---
title: Use cases for business continuity planning
description: This section describes the common use cases that are used for business continuity planning in the Business Continuity Management application. You can deploy these use cases individually or you can combine them to meet your specific needs.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Business continuity planning, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Use cases for business continuity planning

This section describes the common use cases that are used for business continuity planning in the Business Continuity Management application. You can deploy these use cases individually or you can combine them to meet your specific needs.

You can build your business continuity plan based on your recovery strategy, partners, teams, tools, and processes that are needed to implement the plan.

Consider an example of a malware attack on a corporation. The attack may disrupt critical services such as utilities, transportation, payments, and so on. If a business continuity plan is in place, the emergency IT consultants and professionals can implement preventive actions:

-   Shut down the IT services.
-   Restore the services from the disaster data recovery component in the plan.
-   Control the damage by moving the essential data servers to an off-site location.

## Use cases for planning

<table id="table_agg_gq5_bcc"><thead><tr><th>

Use case name

</th><th>

Description

</th><th>

Roles

</th><th>

Actions for the use case

</th></tr></thead><tbody><tr><td>

Create a standardized recovery plan

</td><td>

BCP helps you enact and mitigate risk at the time of an event by addressing action items such as plan assets, activities, recovery teams, documentation, policies, and procedures.

 The plan record goes through a cycle of states before:

 -   Draft -&gt; In review -&gt; Pending approval -&gt; Approved -&gt; Archived
-   In the **Pending approval** state, plan can be rejected back to **Returned** state.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User creates a plan.

</td></tr><tr><td>

Update dependencies in the plan

</td><td>

Update dependencies in the plan: 1. Enables users to view and configure the assets that are affected within the plan.

2. Monitor the RTO, RPO, and Recovery Tier of each asset and identify any gaps/risks when the asset is down.

3. View the relationship of the primary assets and related assets.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User selects Update dependencies button.

 The Update BCP dependencies snapshot scheduled job is executed.

</td></tr><tr><td>

Configure the dependencies for plan

</td><td>

Provide configurations for users to configure what dependencies they want for plans including:

 1.  Configure the sources that they want to pull in from their dependencies including CMDB, BIA downstream, BIA upstream.
2.  Choose whether they want to pull the last updated record or all records from the source.
3.  Configure the users and groups that they want to notify via emails.
4.  Configure the fields that are updated when dependencies are updated.
5.  Configure what type of plans the configurations should be applied to.

</td><td>

BCM administrator

</td><td>

User creates or updates records by navigating to

 All -&gt; Planning dependency update configuration.

</td></tr><tr><td>

Create documentations

</td><td>

Provides a section and templates for the user to document the goals, objectives, and scopes that are required within the context of the plan.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User creates a plan using a plan template with document sections defined.

 User creates a section in the Documentation tab.

</td></tr><tr><td>

Create recovery teams

</td><td>

Defines the teams responsible for executing the plans during the recovery process. It is used in recovery tasks.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User selects New button in the Recovery teams related list.

</td></tr><tr><td>

Monitor the loss scenarios of the plan

</td><td>

Create crisis scenarios that can be included in your plan \(for example, Loss of Datacenters or Vendor disruption\) and add assets dependencies or recovery strategies to the loss scenarios.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User creates a plan using a plan template with loss scenarios defined.

 User adds the loss scenarios.

</td></tr><tr><td>

Submit for approval

</td><td>

Create approval configurations including groups, users, or rules to standardize the approval process.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User submits the plan for approval.

</td></tr><tr><td>

Generate PDF

</td><td>

Summarize the details of the plan \(scopes, asset dependencies, related plans, recovery teams, recovery tasks\) in a PDF format.

 2. Enables users to write scripts and format the PDF through document templates, and document scripts.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User generates PDF of the plan.

</td></tr><tr><td>

Copy plan

</td><td>

Copy existing plans including their details and related lists.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User copies the plan.

</td></tr><tr><td>

Add related plan

</td><td>

Add the related plan to the related list.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User adds a related plan.

</td></tr><tr><td>

Avoid creating cyclic tasks for the same plan while adding plan dependencies.

</td><td>

Stop processing same plan if its already part of the hierarchy. Avoid creation such plan dependencies during planning phase. Verify that plan dependency in recovery task doesn’t create a cycle.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User adds an activated plan to the plan recovery task.

</td></tr><tr><td>

Task execution order

</td><td>

Tasks under a plan can be parallel and sequential based on the task dependencies. Therefore, the tasks in a plan should be ordered.

</td><td>

BCM planner, BCM manager, BCM administrator

</td><td>

User adds recovery tasks.

</td></tr></tbody>
</table>