---
title: Incident Management Best Practice – San Diego
description: The Incident Management Best Practice – San Diego plugin \(com.snc.best\_practice.incident.sandiego\) enhances integration and workflows for incidents and problems. You can use it to update agents and callers on the progress of a reported incident or problem.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/inc-mgmt-best-prac-plugin-sd.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Incident Management plugins, Reference, Incident Management, IT Service Management]
---

# Incident Management Best Practice – San Diego

The Incident Management Best Practice – San Diego plugin \(com.snc.best\_practice.incident.sandiego\) enhances integration and workflows for incidents and problems. You can use it to update agents and callers on the progress of a reported incident or problem.

## Requirements and dependencies

Install these additional plugins to use the Incident Management Best Practice – San Diego plugin:

-   Problem Management Best Practice — Madrid plugin \(com.snc.best\_practice.problem.madrid\).

    For more information on this plugin and the activation process, see [Activate Problem Management Best Practice — Madrid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/problem-management/activate-pm-best-practice-madrid.md).

-   Problem Management Best Practice — Madrid – Knowledge Integration plugin \(com.snc.best\_practice.problem.madrid.knowledge\).

    For more information on this plugin and the activation process, see [Activate Problem Management Best Practice — Madrid — Knowledge Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/problem-management/act-pm-best-prac-madrid-know-int.md).

-   Problem Management Best Practice – Jakarta plugin \(com.snc.best\_practice.problem.jakarta\).

    This plugin is not installed by default for zBoot customers. Install the plugin manually. This plugin controls known error article behavior in the incident or problem workflow. For more information on this plugin and the activation process, see [Activate Problem Management Best Practice — Jakarta](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/problem-management/act-pm-best-prac-jakarta.md).


All these plugins except com.snc.best\_practice.problem.jakarta are active by default for new customers. Existing or upgrading customers must request the plugin or install the plugin manually. For more information, see [Request a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_RequestAPlugin.md).

## Impacts on upgrading customers

If existing or upgrading customers install the Incident Management Best Practice – San Diego plugin \(com.snc.best\_practice.incident.sandiego\), their configured workflows might change. Before you use the plugin in a production environment, install it in a non-production or test environment and test the workflows to verify that they behave as expected.

When the plugin is installed:

-   New options are populated along with the old \(existing or already configured\) options.
-   These files are affected:

    -   Business rule: **Close Code**
    -   ML Solution Definition: Similar Resolved Incidents. Update the filter.
    -   Script Action: **Update Incident when Problem closes**. Update the resolution code to the correct choice.
    **Note:**

    If these items haven't been customized or configured, they're overridden and the new options are populated.

-   Customers must manually remove the old options. If a customer has configured a combination of old and new options, update the affected workflows.

## Enhancements

This plugin enhances the incident and problem workflow to support the following activities:

-   **Create a problem**

    When you create a problem from an existing incident, the incident **State** is set to **On Hold** and the **Reason** is set to **Awaiting Problem** until the linked problem is resolved.

-   **Attach a Known Error \(KE\) article**
    -   When you associate a KE article with the incident and the KE article has an associated problem, the problem is also associated with the incident.
    -   When you select **Known error** as **Resolution code** to resolve an incident but the incident contains no associated KE articles, then the system prompts you to select a KE article.
-   **Communicate Workaround**

    If a workaround is added to the problem, and if you select the **Communicate Workaround** related link, then the following occurs:

    -   The workaround is copied to the **Work notes** field. A notification is sent to the users listed in the **Assigned to** and **Work notes list** fields. The notification is sent only when the incident state is New, On Hold, or In Progress.
    -   The workaround is copied to the **Additional Comments** field. If **Known error** is selected from the **Resolution code** field of the incident, then a notification is sent to the caller and to the users listed in the **Assigned to** and **Watch list** fields.
-   **Communicate Fix**

    If a fix is added to a problem and if you select the **Communicate Fix** related link, then the following occurs:

    -   The fix is copied to the **Work notes** field.
    -   A notification is sent to the users listed in the **Assigned to** and **Work notes list** fields of the problem record. The notification is sent only when the incident state is New, On Hold, or In Progress.

-   **[Activate Incident Management Best Practice – San Diego](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/act-inc-mgmt-best-prac-plugin-sd.md)**  
Activate the Incident Management Best Practice – San Diego plugin \(com.snc.best\_practice.incident.sandiego\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

**Parent Topic:**[Incident Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/incident-mgmt-plugins.md)

