---
title: Guidelines for translated dashboards
description: Users can only find translated dashboards under certain configurations. You can translate the dashboard name to make it searchable. When working with language plugins, refer to these guidelines to make sure users can find your translated dashboards.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Guidelines for translated dashboards

Users can only find translated dashboards under certain configurations. You can translate the dashboard name to make it searchable. When working with language plugins, refer to these guidelines to make sure users can find your translated dashboards.

-   **Overview of translated dashboards**

    On instances with language plugins enabled, the application verifies the instance's database is MySQL, then it looks for the user's session language and searches for the translated dashboard. This topic assumes that at least one additional language plugin is activated.

    The search function only works for translated dashboards when the instance uses the MySQL database and the dashboard translation is provided.

    Learn more: [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

-   **Translate a dashboard's title**

    Open the dashboard, select the target language in your preferences, and in the dashboard's properties, enter the translated name of the dashboard. Other users can now find the dashboard using its localized name.

    Learn more: [Solving issues on translated dashboards](../task/solving-issues-translated-dashboards.md).


