---
title: Default proactive prompts for Manager Hub
description: Default signal configurations, signal categories, and an action URL are available to use on activating Manager Hub and Proactive Prompts.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Reference for Manager Hub, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Default proactive prompts for Manager Hub

Default signal configurations, signal categories, and an action URL are available to use on activating Manager Hub and Proactive Prompts.

To learn how to use Proactive Prompts, refer to the [Proactive Prompts](proactive-prompts-for-hrsd.md) documentation.

## Signal configurations

For detailed information on how to configure signals in Proactive Prompts, see [Configuring Proactive Prompts](proactive-prompts-config.md).

<table id="id_s1t_qps_tvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned learning lack of engagement

</td><td>

Default signal configuration to display the **Support employees with learning** widget in the Manager Hub page.This configuration is available only when the Learning Core application is installed.

 A schedule job runs every two weeks and identifies users based on the following criteria. These users are displayed to the manager in the **Support employees with learning** widget.

-   learning course or path has been assigned by the manager
-   assignment date is one month or more in the past
-   learning course in not in Work in progress or completed state

</td></tr><tr><td>

Time since job change

</td><td>

Default signal configuration to display the **Help your employee grow their career** widget in the Manager Hub page.This configuration is available only when Human Resources Scoped App: Core plugin is installed.

A scheduled job runs every six months and identifies users based on this criterion: 36 months or more since the start date of current job role.

</td></tr><tr><td>

Employee hasn’t taken PTO

</td><td>

Default signal configuration to display the **Encourage work-life balance** widget in the Manager Hub page.This configuration is available only when Human Resources Scoped App: Core plugin is installed.

A scheduled job runs every three months and identifies users using one of the following criteria:

-   time-off balance is 50% or more of the total available and is October 1 or later in the current calendar year
-   last date when the time off was taken was 6 months or more in the past and time off balance is more than zero

</td></tr><tr><td>

New hire above average requests

</td><td>

Default signal configuration to display the **Support your new hire** widget in the Manager Hub page.This configuration is available only when the Human Resources Scoped App: Core plugin is installed.

A scheduled job runs every 14 days to identify users based on the following criteria:

-   employee start date is 30 days or less in the past
-   employee has opened six or more requests in the past 14 days
-   requests are either HR case \(except life cycle event case\), or catalog item is software or hardware request, or a single request of high priority
-   requests are not closed complete

</td></tr><tr><td>



</td><td>



</td></tr><tr><td>



</td><td>



</td></tr><tr><td>



</td><td>



</td></tr><tr><td>



</td><td>



</td></tr></tbody>
</table>## Signal categories

Signal categories are the logical groups to divide signals. Signal categories enable you to pull category-specific prompts on the prompt widget.

Career, Employee service, New hire, Team insights, and Well-being are the default signal categories that are available for Manager Hub. For more information on these signal categories, see [Configure signal categories in Proactive Prompts](../task/proactive-prompts-signal-catergories.md).

## Signal actions

Signal actions enable end users who receive the prompt to act on them. **Open a URL** is the default signal action that is available for Manager Hub.

For more information on signal actions, see [Configure signal actions for Proactive Prompts](../task/proactive-prompts-signal-actions.md).

**Parent Topic:**[Reference for Manager Hub](../reference/reference-manager-hub.md)

**Related topics**  


[Components installed with Manager Hub](../reference/installed-with-managerhub.md)

[Campaign configurations for Manager Hub](manager-hub-campaign.md)

[Default configurations for important dates](manager-hub-imp-dates.md)

[Default configurations for team requests](manager-hub-team-requests.md)

[Default configurations for team data](team-data-config.md)

[Default configurations for team column data](config-team-column.md)

[Default configurations for filter groups](config-filter-group.md)

[Default configurations for daily stats](config-daily-stats.md)

[Default configurations for To do's](manager-hub-todos.md)

[Use the View menu icon in Manager Hub](../reference/view-menu.md)

[Assign learning form](../reference/assign-learning-form.md)

[Create a conversation form](../reference/create-conversation-form.md)

[Schedule a conversation form](../reference/schedule-conversation-form.md)

