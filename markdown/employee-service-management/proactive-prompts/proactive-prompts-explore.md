---
title: Exploring Proactive Prompts
description: Learn how to use the Proactive Prompts application in your organization, configuring the signal for prompts, generating the prompts, and displaying them with actions on the selected channels.
locale: en-US
release: yokohama
product: Proactive Prompts
classification: proactive-prompts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Exploring Proactive Prompts

Learn how to use the Proactive Prompts application in your organization, configuring the signal for prompts, generating the prompts, and displaying them with actions on the selected channels.

## Proactive Prompts workflow

A scheduled job triggers the Proactive Prompts script that evaluates the signal configuration. Signal configuration contains two parts:

-   Signal details such as to whom to send the prompt, on which channels, what actions are made available, and templates for the prompt message displayed to the user.
-   Signal data source that contains data tables and conditions.

Prompts are then generated and sent to configured platforms like Service Portal, Microsoft Teams, Slack, or Virtual Agent.

The following image illustrates this Proactive Prompts workflow.

![Proactive Prompts workflow](../image/proactive-prompts-overview.png)

## Channels in Proactive Prompts

Channels are the medium through which prompts are displayed to the end user in their flow of work.

The following table describes the channels available in Proactive Prompts.

<table id="table_z55_pnt_vvb"><thead><tr><th>

Channels

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Portal widget

</td><td>

Prompts are displayed through a widget on the Employee Portal.**Note:** To see the prompts on the portal, the Prompt widget must be added to the portal page. For information on configuring portal pages, see [Create and edit a page using the Service Portal Designer](https://www.servicenow.com/docs/access?context=t_ConfigureAPage&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US). For information on adding widgets to a page, see [Service Portal widgets](https://www.servicenow.com/docs/access?context=service-portal-widgets&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Virtual Agent

</td><td>

Prompts can also be delivered to different Conversational Interface \(CI\) channels through Virtual Agent, for example, Microsoft Teams or Slack.

</td></tr></tbody>
</table>**Note:** For more information, see [Configure delivery channels in Proactive Prompts](../task/proactive-prompts-config-channels.md).

## Configuring data

Configure signals, data sources, channels, categories, actions, and schedules to display prompts to managers and employees in their flow of work. For more information, see [Configuring Proactive Prompts](proactive-prompts-config.md).

## Proactive Prompts in Manager Hub

Generate and display micro insights to managers using Manager Hub through Proactive Prompts. The insights contain reminders about the team's service requests, journeys, and learnings, accompanied by relevant actions to communicate the information to the employees. For more information, see [Proactive Prompts for managers](../task/insight-based-sug.md).

