---
title: AI Search event and action logs for AI Search usage in Recommended Actions
description: AI search event and action logs capture user interactions and search activities, providing data for AI search analytics dashboards.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [AI search, event logging, analytics, ServiceNow, AI Search event logs and Analytics, AI search usage using the AI search analytics dashboard, Tracking the AI search usage in Recommended Actions]
breadcrumb: [AI search, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# AI Search event and action logs for AI Search usage in Recommended Actions

AI search event and action logs capture user interactions and search activities, providing data for AI search analytics dashboards.

## Search event and action logs

The logging of search-related events within a search system focuses on how search queries, results, and user interactions are recorded in various tables for analytics purposes.

-   Search event logging: The search events logging, including search queries, results, and user actions, by queuing events and processing them into dedicated tables. The search events are queued in the Queued Signal Events table first and then when they’re processed, they’re moved into the search events table.
-   Event logging triggers: The search events, search source events, and search signal events tables capture details like query changes, sources of results, and applied facet filters. The logging occurs not only when searches happen but also when filters, facets, or sorts are applied, ensuring comprehensive capture of user interactions with search features.

    Events are queued and then processed into the following tables:

    -   Search Events table \[sys\_search\_event\]: Logs search queries, user info, and result status.
    -   Search Source Events table \[sys\_search\_source\_event\]: Captures the origin of the query \(for example, catalog item\).
    -   Search Signal Events table \[sys\_search\_signal\_event\]: Logs facet filters the facet filters applied on the results for a search query and source mappings.
    For more information on the preceding tables, see Search Suggestions tables.

-   Search result action logging: Separate tables exist for logging clicks and actions on search results, including distinctions between normal and genius result actions, with multiple entries for multiple actions on a single source. When you interact with a search result, such as clicking on a link or performing an action, these actions are recorded. For the preview experience, actions like drill down are automatically logged to avoid duplication. This data is then used to populate analytics dashboards, either prebuilt or custom, enabling you to track and analyze the interactions with search results effectively.

    For custom guidances, you must emit the log search result event with the appropriate payload structure, which includes action-related data. Emitting action details in the payload is optional. Without it, events are still logged but lack specific action information, preventing duplication by using unique action IDs. Custom guidance actions require emitting events with a provided payload structure to log action details, while out-of-the-box guidances handle this automatically. For payload structure, see [Custom action log payload structure](ra-ai-search-event-logs.md#custom-action-logging-payload-structure).

    -   Search Result Events table \[sys\_search\_signal\_result\_event\]: Stores signal data for search results that you select.
    -   Search Result Event Actions table \[sys\_search\_signal\_result\_event\_action\]: Stores signal data for user interactions with search results.
    -   Genius Result Actions table \[sys\_search\_genius\_result\_event\_action\]: Stores signal data for user interactions with Genius Result answer cards.
    For more information on the preceding tables, see Search signal tables.

-   AI search analytics: The logged data is then used to populate the AI search analytics dashboards, either prebuilt or custom, enabling you to track and analyze the interactions with search results effectively. For more information on the AI search analytics dashboard, see AI Search analytics dashboard. You can view the CSM workspace-related AI Search usage within Recommended Actions in the AI Search Analytics dashboard by selecting the **\[CSM AIS\] Configurable Workspace Search Config** option in the application drop-down on the top-right.

## Custom action log payload structure

For custom action logging, that is, for the action you create on a guidance preview experience, you must emit an event with a payload structure that includes action-related data. Other common fields such as applied filters and views are handled by the system. If the payload is empty, the event will still be logged, but the action details won’t be available. This structured payload is crucial for building detailed analytics dashboards, as it provides specific information about user interactions with custom actions.

```
api.emit(LOG_SEARCH_RESULT_EVENT, {actionData: {actionName: actionId}})
```

For more details on how to configure the payload for custom actions, see [Customize a guidance preview experience in the UI Builder](../task/customize-ra-preview-experience.md).

