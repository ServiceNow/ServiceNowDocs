---
title: Incident Management Best Practice – San Diego
description: The Incident management best practice -San Diego plugin \(com.snc.best\_practice.incident.sandiego\) enhances the integration and workflows for incidents and problems. This plugin enables you to update the progress of the reported incident and problem to the agent and caller.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Incident Management plugins, Reference section for Incident Management, Incident Management, IT Service Management]
---

# Incident Management Best Practice – San Diego

The Incident management best practice -San Diego plugin \(com.snc.best\_practice.incident.sandiego\) enhances the integration and workflows for incidents and problems. This plugin enables you to update the progress of the reported incident and problem to the agent and caller.

## Requirements and dependencies

Install these additional plugins to use the Incident management best practice — San Diego plugin:

-   Problem Management Best Practice — Madrid plugin \(com.snc.best\_practice.problem.madrid\).

    For more information on this plugin and the activation process, see [Activate Problem Management Best Practice — Madrid](../../problem-management/task/activate-pm-best-practice-madrid.md).

-   Problem Management Best Practice — Madrid – Knowledge Integration plugin \(com.snc.best\_practice.problem.madrid.knowledge\).

    For more information on this plugin and the activation process, see [Activate Problem Management Best Practice — Madrid — Knowledge Integration](../../problem-management/task/act-pm-best-prac-madrid-know-int.md).

-   Problem Management Best Practice – Jakarta plugin \(com.snc.best\_practice.problem.jakarta\).

    This plugin is not installed by default for zBoot customers. Install the plugin manually. This plugin is responsible for known error article behavior in the incident or problem workflow. For more information on this plugin and the activation process, see [Activate Problem Management Best Practice — Jakarta](../../problem-management/task/act-pm-best-prac-jakarta.md).


All the plugins except for com.snc.best\_practice.problem.jakarta are activated by default for the new customers. Existing or upgrading customers must request the plugin or install the plugin manually. For more information, see [Request a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_RequestAPlugin.md).

## Impacts on upgrading customers

For the existing or upgrade customers, if they install the Incident management best practice -San Diego \(com.snc.best\_practice.incident.sandiego\) plugin, the existing configured workflows might get changed. If the customer wants to install the plugin, they must install the plugin in the sub-production or testing environment and test the workflows before using the plugin in the production environment to ensure the desired workflow is maintained.

When the plugin is installed:

-   New options are populated along with the old \(existing or already configured\) options.
-   These files are affected:

    -   Business rule: Close Code
    -   ML Solution Definition: Similar Resolved Incidents -&gt; The Filter must be updated
    -   Script Action: Update Incident when Problem closes -&gt; Update the resolution code to proper choice
    **Note:** Files are overridden if no customizations or configurations are done. In such case, new options are populated.

-   Customer must manually remove the old \(existing\) options. If customer has configured a combination of the old \(existing\) and new options, then the necessary workflows must be updated.

## Enhancements

This plugin enhances the incident and problem workflow to support the following activities:

-   **Create a problem**

    When you create a problem from an existing incident, the incident **State** is set to **On Hold** and the **Reason** is set to **Awaiting Problem** until the linked problem is resolved.

-   **Attach a Known Error \(KE\) article**
    -   When you associate a Known Error \(KE\) article to the incident, and if the KE article has a problem associated to it, then the problem also gets associated with the incident.
    -   When you select **Known error** as **Resolution code** to resolve an incident but the incident contains no associated KE articles, then the system prompts you to select a KE article.
-   **Communicate Workaround**

    If a workaround is added to the problem, and if you click the **Communicate Workaround** related link, then the following occurs:

    -   The workaround is copied to the **Work notes** field. A notification is sent to the users listed in the **Assigned to** and **Work notes list** fields. The notification is sent only when the incident state is New, On Hold, or In Progress.
    -   The workaround is copied to the **Additional Comments** field. If **Known error** is selected from the **Resolution code** field of the incident, then a notification is sent to the caller and to the users listed in the **Assigned to** and **Watch list** fields.
-   **Communicate Fix**

    If a fix is added to a problem and if you click the **Communicate Fix** related link, then the following occurs:

    -   The fix is copied to the **Work Notes** field.
    -   A notification is sent to the users listed in the **Assigned to** and **Work notes list** fields of the problem record. The notification is sent only when the incident state is New, On Hold, or In Progress.

-   **[Activate Incident Management Best Practice – San Diego](../task/act-inc-mgmt-best-prac-plugin-sd.md)**  
Activate the Incident Management Best Practice — San Diego plugin \(com.snc.best\_practice.incident.sandiego\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

**Parent Topic:**[Incident Management plugins](incident-mgmt-plugins.md)

