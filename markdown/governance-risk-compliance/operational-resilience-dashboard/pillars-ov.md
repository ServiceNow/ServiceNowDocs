---
title: Pillars overview tab
description: A pillar is a foundational element that supports your organization's operational resilience. You can map business services and processes to these pillars in the Operational Resilience application to establish relationships and monitor their status on the dashboard in the Operational Resilience Workspace.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Landing page and dashboard views, Operational Resilience, Governance, Risk, and Compliance]
---

# Pillars overview tab

A pillar is a foundational element that supports your organization's operational resilience. You can map business services and processes to these pillars in the Operational Resilience application to establish relationships and monitor their status on the dashboard in the Operational Resilience Workspace.

## Pillars overview tab on the landing page

The **Pillars overview** tab on the landing page of the Operational Resilience Workspace provides information on the pillars, which are part of the base system in Operational Resilience. From the dashboard, you can monitor the status of the services for each pillar. The Pillars overview section displays data filtered for the selected pillar as shown in the example.

![Pillars overview.](../../grc-operational-res/image/p-ov-hp.png)

## Tables associated with the Pillars overview tab

The following table lists all the tables that are associated with each section of the **Pillars overview** tab report.

<table id="table_rfd_rfm_cfc"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Pillars

</td></tr><tr><td>

Dependencies

</td><td>

Dependencies for the pillar. Source table for this report: Dependencies \[sn\_oper\_res\_profile\]

</td></tr><tr><td>

Supported services

</td><td>

Supported services for the pillar. Source table for this report: \[sn\_oper\_res\_profile\]

</td></tr><tr><td>

Supported business services

</td><td>

Supported business services for the pillar.Source table for this report:\[sn\_oper\_res\_profile\]

</td></tr><tr><td class="sub-head" colspan="2">

Red flags

</td></tr><tr><td>

Major open incidents

</td><td>

Major open incidents for the pillar. Source table for incidents: Incidents \[sn\_oper\_res\_incident\]

</td></tr><tr><td>

Risk rating

</td><td>

Source table for risks: Risks \[sn\_oper\_res\_risk\]

</td></tr><tr><td>

Control effectiveness

</td><td>

Source table for failed controls: Failed Controls \[sn\_oper\_res\_failed\_control\]

</td></tr><tr><td>

Issues

</td><td>

Source table for issues: Issue \[sn\_oper\_res\_issue\]

</td></tr><tr><td class="sub-head" colspan="2">

Suggestions

</td></tr><tr><td>

Top Controls to be Strengthened

</td><td>

Failing controls that impact the most critical services. Source table for this report: Services with Failed Controls \[sn\_oper\_res\_failed\_control\]

</td></tr><tr><td>

Top Risks to be Mitigated

</td><td>

Top risks threatening your organization compared with your impacted services. This report can be useful for determining where to start your mitigation efforts and in what areas you should devote the most resources around implementing controls.Source table for this report: Services with High Risks \[sn\_oper\_res\_risk\]

</td></tr><tr><td>

Top vulnerabilities to be fixed

</td><td>

Top vulnerabilities to be fixed for the services.

</td></tr></tbody>
</table>You can view data for the following pillars from the dashboard:

-   Application Service
-   Business Services
-   Data
-   Facilities
-   People
-   Process
-   Services
-   Service offering
-   Suppliers
-   Technology

The following sample report shows data for the Application Service pillar with its precise metrics.

-   Dependencies
-   Supported services
-   Supported business services

![Overview.](../../grc-operational-res/image/p-ov.png)

## Report on the red flags

The Red flags report on the **Pillars overview** tab shows the total number of red flags that require immediate attention for the associated assets, controls, issues, and risks related to the selected pillar. It breaks down details of the red flags based on the integrations with the Operational Resilience application. For example, if you have installed the Risk Management application, data for the risk ratings is pulled from that application and displayed in this report.

If you install the optional applications from the GRC product suite, such as Business Continuity Management and Vulnerability Response in your instance, you can also view the Business Continuity plan and Vulnerability Response reports on the dashboard.

A sample Red flags report for the pillars is shown in the example.

![Red flags.](../../grc-operational-res/image/p-red-flags.png)

The following data is displayed for the pillars in the Red flags report:

-   Assets without business continuity plans and Assets not recovered in recent DR exercise: These red flags are shown for the selected pillar in the example as the Operational Resilience application is integrated with the BCM application.
-   Major open incidents
-   Scores for Risk rating, Control effectiveness, and Issues

## Suggestions for mitigating the issues

The Suggestions report on the **Pillars overview** tab offers recommendations and workarounds to mitigate issues and risks for various resilience metrics associated with the pillar.

![Suggestions.](../../grc-operational-res/image/p-suggestions.png)

Depending on the applications integrated with Operational Resilience, suggestions are displayed in the report. For example, if you have installed the Policy and Compliance Management, Risk Management, and Vulnerability Response applications, the following suggestions are displayed in the report.

-   Top controls to be strengthened
-   Top risks to be mitigated
-   Top vulnerabilities to be fixed

For more information on the pillars in Operational Resilience, see [Exploring Operational Resilience](../../grc-operational-res/concept/what-is-opres.md).

