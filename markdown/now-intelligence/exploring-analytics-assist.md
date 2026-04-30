---
title: Exploring Analytics Generation
description: Use Analytics Generation to generate Platform Analytics artifacts from conversational interactions. For example, you can ask for information about the number of open incidents and get a single-score data visualization.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Analytics Generation, Platform Analytics]
---

# Exploring Analytics Generation

Use Analytics Generation to generate Platform Analytics artifacts from conversational interactions. For example, you can ask for information about the number of open incidents and get a single-score data visualization.

## Overview of Analytics Generation

Analytics Generation currently contains the data visualization generation skill. The data visualization generation skill lets your developers create relevant charts and scores based upon natural language queries and available data, leveraging Platform Analytics. The charts can show data from any ServiceNow AI Platform tables. The user can add the visualization to a dashboard. This skill simplifies the process of data visualization generation and configuration, potentially increasing efficiency.

## Roles

The now.assist.creator and now\_assist\_panel\_user roles are required to use Analytics Generation. The user must also have access to the data for which they are requesting a visualization.

The admin role is required to configure Analytics Generation.

The user can add a generated visualization to any dashboard to which they have editing rights, regardless of role.

## Activation

Analytics Generation is installed with the Now Assist for Creator \(sn\_now\_creator\) application. You can install this application from the ServiceNow Store website.

## Supported Now Assist skills

Analytics Generation currently supports only the data visualization generation skill.

## Supported user interfaces

Access the data visualization generation skill by starting a conversation in Now Assist and asking for information available from a Platform Analytics data source.

![Query asking Now Assist to show all indicators that have not been resolved for over 30 days.](../image/nowass-dv-intro.png "Asking Now Assist for a data visualization")

![Result of the query showing a list of indicators.](../image/nowass-dv-list.png "Example of a generated data visualization")

**Parent Topic:**[Analytics Generation](../reference/analytics-assist-landing-page.md)

