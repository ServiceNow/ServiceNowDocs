---
title: Event Management release notes
description: The ServiceNow Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management provides alert aggregation for discovered services, application services, and automated alert groups. Event Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
---

# Event Management release notes

The ServiceNow® Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management provides alert aggregation for discovered services, application services, and automated alert groups. Event Management was enhanced and updated in the Xanadu release.

## Event Management highlights for the Xanadu release

-   Visualize the chain of events that caused an issue by viewing an alert group timeline in Express List.
-   Understand the connection between the alerts by using Alert Assist's AI-driven technical analysis on alert groups.
-   Use the enhanced service map for alert impact visualization in Service Operations Workspace and Express List.

-   Select all alerts in Express List to perform bulk actions.
-   Remove alerts from an alerts group in Express List.
-   Hide closed alerts in Express List.
-   View data on Impacted Services in the preview panel in Express List.
-   Create an incident with an AI-generated summary from alerts in Express List.
-   View data on configuration items \(CIs\) on the preview panel in Express List.
-   Optimize alert resolution with AI-driven investigation of past related incidents by Now Assist.
-   Generate an alert group description in Express List using Now Assist.
-   Launch an alert analysis from the Now Assist panel.

See [Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Customize the default order of the alert correlation algorithm](https://www.servicenow.com/docs/access?context=Alert-Groups&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Configure the alert correlation algorithm sequence by customizing it according to your needs.

-   **[Create team-based alert management rules](https://www.servicenow.com/docs/access?context=alert-management-rule&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Assign alert management rules to specific assignment groups so that only those alerts that are assigned to the specified group are executed.

-   **[Create tag based alert clustering definitions by teams](https://www.servicenow.com/docs/access?context=alert-clustering-definitions&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Create tag clusters only for alerts that are assigned to an alert group by assigning tag-based alert clusters to specific groups.

-   **[Restrict alert groups across alert assignment groups](https://www.servicenow.com/docs/access?context=alert-filtering&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Improve the accuracy and relevance of the alert correlation by grouping alerts according to a diverse set of requirements.

-   **[Scale out for alert group creation](https://www.servicenow.com/docs/access?context=Alert-Groups&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Ensure efficiency when running a job during high-alert traffic by scaling out the alert grouping job.

-   **[View unified service map and the impact paths in Service Operations Workspace](https://www.servicenow.com/docs/access?context=view-impact-tree&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Explore the updated service map in the Service Operations Workspace, designed to focus on the path that was affected by an alert to help you quickly assess its impact on a service. The map displays all configuration items \(CIs\) for services with up to 60 CIs, regardless of alert status. For services with over 60 CIs that have alerts, it shows the path of the most severe, most recent alert. You can also investigate an even broader view of the service topology. Access the service map directly from Service Operations Workspace, or through the preview panel or an impacted service in Express List.

-   **[Perform bulk actions on alerts in Express List](https://www.servicenow.com/docs/access?context=acknowledge-alerts&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Perform an action on up to 1,000 alerts in the Active alerts list simultaneously.

-   **[Remove alerts from an alerts group in Express List](https://www.servicenow.com/docs/access?context=el-remove-alerts-from-group&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Remove secondary alerts from an alert group directly from the Express List pane or from the preview panel.

-   **[Hide closed alerts on the preview panel and in Link View in Express List](https://www.servicenow.com/docs/access?context=el-hide-closed-alerts&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    View only the open alerts on the preview panel and in Link View in Express List by toggling to hide the closed alerts.

-   **[View data on impacted services on the preview panel in Express List](https://www.servicenow.com/docs/access?context=el-impacted-services-data&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    View information about Impacted Services on the preview panel and in Link View in Express List and open the Service Map and Metric Explorer directly from the panel.

-   **[Create an incident with Now Assist in Express List](https://www.servicenow.com/docs/access?context=el-create-incident-now-assist&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Generate incidents from alerts in Express List with a summary created by genAI that includes details on configuration items and impacted services.

-   **[View data on configuration items on the preview panel in Express List](https://www.servicenow.com/docs/access?context=el-ci-data&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.

-   **[Speed up alert resolution with a Now Assist analysis of past related incidents](https://www.servicenow.com/docs/access?context=nai-past-incidents&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Enhance efficiency and reduce downtime with a Now Assist analysis of past incidents on the same or related CIs. Now Assist investigates historical data to identify past incidents related to the current alert and reports their frequency and criticality levels. It also provides a summary of effective strategies used to resolve them. In addition, Now Assist offers contact information for individuals or teams who have resolved similar incidents in the past and could assist when needed.

-   **[Generate an alert group description in Express List using Now Assist](https://www.servicenow.com/docs/access?context=alert-group-descr-generate-el&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Use Now Assist to generate a description of an alert group in Express List that encompasses all the alerts within the group. The generated description replaces the original description of the group.

-   **[Launch an alert analysis from the Now Assist panel](https://www.servicenow.com/docs/access?context=alert-analysis-now-assist-panel&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Analyze an alert from the Now Assist panel. The alert analysis displays directly in the Now Assist panel for convenient review.


## Changed in this release

-   **[Alert page performance enhancements](https://www.servicenow.com/docs/access?context=c_EMAlert&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Benefit from the enhanced load time of the alert forms and service dashboard.

-   **[Calculate impact during loop dependency](https://www.servicenow.com/docs/access?context=cross-business-service-impact&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Support for circular \(loop\) dependency between configuration items in the impact tree is enabled.

-   **[Automated alert groups perform tag-based alert clustering](https://www.servicenow.com/docs/access?context=c_SACorrelatedAlertGroups&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Tag-based alert group correlation is performed as part of automated alert groups.


## Removed in this release

The Event Management Mobile application is no longer available.

## Deprecations

The following dashboards have been deprecated:

-   Event Management scorecards
-   Event Management insights
-   Event Management overview
-   Health Log Analytics Overview

The Service Management dashboard is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article [\(KB0867184\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) in the Now Support knowledge base.

## Activation information

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://www.servicenow.com/docs/access?context=t_EMActivatePlugin&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Metric Explorer](https://www.servicenow.com/docs/access?context=agent-workspace-ops-intelligence&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    ServiceNow® Agent Workspace for [Metric Intelligence](https://www.servicenow.com/docs/access?context=operational-metrics&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) provides a central interface that enables you to view the health of a CI associated with an alert. Health details for a CI include various metric charts with control bounds and aggregations for single score charts.

-   **[Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The ServiceNow® Now Assist for IT Operations Management \(ITOM\) application analyzes alerts in Event Management. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.


**Parent Topic:**[ITOM Health release notes](itom-health-rn.md)

