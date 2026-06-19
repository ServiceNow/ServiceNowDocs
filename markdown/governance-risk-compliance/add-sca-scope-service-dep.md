---
title: Define the scope and dependencies
description: Define the scope of the Scenario analysis by selecting the service to analyze and adding the dependencies that support it during a disruption.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-sca-scope-service-dep.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Scenario Analysis, Operational Resilience, scope, service, dependencies, resilience map]
breadcrumb: [Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Define the scope and dependencies

Define the scope of the Scenario analysis by selecting the service to analyze and adding the dependencies that support it during a disruption.

## Before you begin

Role required: **sn\_oper\_res.admin**, **sn\_oper\_res.manager**

## About this task

The Scope step consists of two sub-steps: adding a service and adding dependencies. Both sub-steps must be completed before advancing to the next playbook step. Once the **Dependencies** sub-step is marked complete, the selected dependencies cannot be changed.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Scenario Analysis** and open the scenario analysis record form.

2.  In the Playbook stage panel, select **Scope**, then select **Services**.

3.  To open the **Select Services** dialog, select **Add**.

    An information banner is displayed in the Select Services dialog.

    **Note:** Only one service can be added as shown in the example; to change it later you must create another scenario analysis record.

    \[Omitted image "sca-add-service.png"\] Alt text: Service selection dialog with the information banner, a single service row 'Retail Banking' selected, and the Add button enabled.

4.  Browse or search by **Name**, **Owner**, **Business Criticality**, **Operational Status**, or **Class**.

    \[Omitted image "sca-service-mapping-msg.png"\] Alt text: Service mapping.

5.  Select the service, then select **Add**.

    The service appears in the Services table with its Impact Tolerance columns populated. Because you can add only one service, the **Remove** button for the service becomes inactive after the service is added.

    \[Omitted image "sca-scope-services-stage.png"\] Alt text: Services table on the Scope step showing one selected service with Business criticality, Impact tolerance Duration, and Financial Impact columns populated.

6.  Select **Continue** to advance to Dependencies.

7.  In the Playbook stage panel, select **Dependencies** under **Scope**.

8.  Choose the source of dependencies from the picker, then select dependencies, and select **Add**.

    1.  Use **Selected dependencies** to scope the analysis to the existing dependency map.

        This is the default option. It lists only the dependencies already related to the service that is in the scope.

    2.  Use **All dependencies** option when you need to bring in a dependency that is not yet related to the service.

        It lists every dependency available in the instance, regardless of whether it is related to the selected service.

    \[Omitted image "sca-dependencies-banner-and-all-dropdown.png"\] Alt text: Dependencies sub-step with the warning banner 'Once you complete this step, the selected dependencies cannot be changed' and the Dependencies dropdown open showing the 'All dependencies' option.

    The selection pop-up is paginated and shows the columns **Name**, **Owner**, **Class**, **Appetite status**, and **Pillar**. Filter and sort controls are available. Selections made across multiple pages are retained when you select **Add**.

    \[Omitted image "sca-dependencies-selection-dialog.png"\] Alt text: Dependencies selection dialog showing Name, Owner, Class, Appetite status, and Pillar columns with row checkboxes; the paginator shows 1–20 of 267 records.

9.  Review the list to confirm that all critical dependencies are included.

    Each row shows the **Dependency** name and its **Pillar**, for example Processes \(Account Opening Workflow, Account Closure Handling, Closure Request Handler\) or Application Services \(Core Banking Portal\). A warning banner is displayed on the Dependencies step: `Once you complete this step, the selected dependencies cannot be changed.`

    \[Omitted image "sca-dep-added.png"\] Alt text: Dependencies step after four dependencies are added, with two columns — Dependency and Pillar — populated. \[Omitted image "sca-dependencies-complete-state.png"\] Alt text: Dependencies sub-step in the Complete state, with the Scope badge updated to Complete in the stage panel.

10. Select **Mark as complete**.

    **Note:** Once you mark this step as complete, the selected dependencies cannot be changed.

    The **Scope** step shows a completed status in the stage panel.


## Result

The **Scope** step is complete. The selected service and its dependencies are locked and are used for scenario testing.

## What to do next

To add scenarios and review reference data such as incidents, see [Add scenarios and review reference data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-sca-scenarios-review-refdata.md).

