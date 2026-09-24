---
title: Service Operations Workspace release notes
description: The Service Operations Workspace application centralizes IT operations, giving real-time snapshots of alerts, workload, and AI impact. Express List speeds monitoring, Integrations Launchpad unifies data, automations cut manual effort, and AIOps dashboards track service health. See the following sections for release notes by version.This release gives AIOps managers and AI specialists new navigation, homepage filtering, standardized workflow monitoring, and broader specialist scope—so teams investigate faster and oversee more from one place.In Express list, you can now switch alert modes without searching and see the reasoning behind each auto-closed alert.Set up connectors faster with conversational Otto configuration and inline credentials, keep them running with clearer activation and error troubleshooting, and rely on modernized vRealize and Dynatrace integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/service-operations-workspace-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Event Management release notes, ITOM AIOps release notes, IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Service Operations Workspace release notes

The Service Operations Workspace application centralizes IT operations, giving real-time snapshots of alerts, workload, and AI impact. Express List speeds monitoring, Integrations Launchpad unifies data, automations cut manual effort, and AIOps dashboards track service health. See the following sections for release notes by version.

## About Service Operations Workspace

-   Monitor your team's command center in real-time, tracking alert activity, workload distribution, and AI's impact on resolution speed.
-   Gain unified visibility across your infrastructure by consolidating events, metrics, and logs through the Integrations Launchpad.
-   Respond proactively to issues by tracking KPIs and service health through comprehensive AIOps dashboards.
-   Reduce alert noise and speed resolution by automatically grouping, enriching, and responding to alerts with automations that minimize manual intervention.

See [Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/sow-landing-page-itom.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Service Operations Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


## Accessibility and localization

-   **Localization information**

    The current available languages for Service Operations Workspace are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.


**Parent Topic:**[Event Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/event-management-rn-static.md)

## AIOps September Store

This release gives AIOps managers and AI specialists new navigation, homepage filtering, standardized workflow monitoring, and broader specialist scope—so teams investigate faster and oversee more from one place.

### What's new

-   **[New navigation to the AIOps Managers home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-operations-workspace-ui-itom.md)**

    Navigate to AIOps Managers home page through **All** &gt; **AIOps Managers**, where you can onboard new specialists and manage them in one place.

-   **[Monitor agentic workflows with the AI Processing Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/use-ai-insights-express-list.md)**

    Monitor, supervise, and control agentic workflows from one standardized interface. View each workflow's execution state and steps, access its reasoning, and step in to intervene when needed.

-   **[Navigate to filtered alerts from the AI Supervising tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-operations-workspace-ui-itom.md)**

    Navigate to Express List by selecting the action link in each tile on the **AI Supervising** tab. This way, you can investigate alerts faster, as the filters are pre-applied to match the alert category.

-   **[Filter AIOps Manager homepage alerts by assignment group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-operations-workspace-ui-itom.md)**

    Oversee multiple teams using a multi-select assignment group filter on the AIOps Manager homepage. Filter by groups you manage, groups you belong to, and unassigned alerts.


### What's changed

-   **[Configure alert grouping automation with AI from Alert Automation pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/group-alert-sow-itom.md)**

    Launch the AI agent for alert grouping directly from Alert Automation pages. Select **Configure with AI** to open the ServiceNow Otto panel with a pre-populated prompt that guides rule creation.

-   **Assign AI Specialists to all groups**

    Assign the AI Specialist to the new **All Groups** option to let it handle alerts from every assignment group. Previously, only the **Add specialist to specific group\(s\)** option was available, which limited the specialist to the groups you chose.


## Express List September Store

In Express list, you can now switch alert modes without searching and see the reasoning behind each auto-closed alert.

### What's new

-   **[Alert auto-closure reasoning and transparency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/reopen-ai-closed-alert.md)**

    See the decision, reasoning, and supporting evidence for each auto-closed alert, including insignificance reasoning and execution traces, so you can verify autonomous closures.


### What's changed

-   **[Express List mode switching without searching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/express-list.md)**

    Change the Express List view between **Essential** and **Extended** mode independently of any search parameter. The list updates immediately to reflect the selected mode, and when you add a search value, results return according to the already-selected mode.


## Integrations Launchpad September Store

Set up connectors faster with conversational Otto configuration and inline credentials, keep them running with clearer activation and error troubleshooting, and rely on modernized vRealize and Dynatrace integrations.

### What's new

-   **[Conversational connector setup with ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/pull-connector.md)**

    Configure vCenter, NagiosXI, SolarWinds, SCOM, and Zabbix by chatting with Otto in a side panel. You set them up without working through manual configuration fields.

-   **[Activation prompt for pull connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/pull-connector.md)**

    Activate the connector from the modal that appears after a connection test passes. It stays open until you act, so you don't forget to activate.

-   **[Push connector error details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/push-connector.md)**

    View the last error message, timestamp, and detailed payload for a push connector. You diagnose and fix failures without leaving the Integration Launchpad.

-   **[Dynatrace Grail problem events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/dynatrace-advanced-settings-fields.md)**

    Create ServiceNow alerts from Dynatrace Grail problem events, with the root-cause entity, all affected CIs, a matching severity, and the problem's current lifecycle status already included. You see the cause and scope up front, so you can respond without investigating from scratch. This connector replaces the classic Dynatrace event integration.

-   **[JSON API support for vRealize](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/t_EMConfigurevRealizeConnectorJS.md)**

    Connect vRealize through the JSON-based API. The connector keeps working on future VMware versions. XML remains supported.


### What's changed

-   **[Credential setup for push connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/push-connector.md)**

    Select or generate a credential—Basic, API key, or OAuth—directly in the setup form, with API key now added as a new option. You configure the inbound endpoint in one place, without provisioning credentials elsewhere.


### What's deprecated or removed

-   **[Classic Dynatrace event integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/dynatrace-advanced-settings-fields.md)**

    Replaced by the new Dynatrace Grail connector. Move to the Grail connector to keep receiving Dynatrace alerts.

-   **[Auto-dismissing success banner \(pull connectors\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/pull-connector.md)**

    Replaced by a persistent activation modal after a passing connection test.


