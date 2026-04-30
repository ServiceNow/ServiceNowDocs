---
title: Manage security threats using the Security Analyst Workspace
description: Security Incident Response includes a new user interface called the Security Analyst Workspace that features powerful tools for assisting in analysis, including the playbook, peek view, and tabs for working on multiple security incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Manage security threats using the Security Analyst Workspace

Security Incident Response includes a new user interface called the Security Analyst Workspace that features powerful tools for assisting in analysis, including the playbook, peek view, and tabs for working on multiple security incidents.

Purpose-built for security analysts, the powerful tools in the Security Analyst Workspace allow you to analyze the ever-growing volume of data associated with security incidents. And automated actions significantly reduce the security incident investigation time, which can be the difference between stopping an attack and suffering a breach.

## Before using the Security Analyst Workspace

Before you can begin using the Security Analyst Workspace, you must ensure that your instance has at least London Patch 3 installed, you have the correct roles defined, and have [downloaded the Security Incident Response UI application from the ServiceNow Store](../task/install-and-configure-new-ui.md).

**Note:** If your instance is running a version earlier than London Patch 3, you must request the Security Incident Response UI plugin through the HI Customer Service system.

## Access the Security Analyst Workspace

To access this new workspace, navigate to **Security Incident** &gt; **Incidents \(New UI\)**.

![Security Incident navigation bar](../image/nav-bar.png "Security Incident")

The workspace opens in a separate browser tab.

![All open Security Incidents](../image/new-ui.png "Security incidents")

## Locate the security incidents you want to analyze with Quick Filters

The Security Analyst Workspace provides several tools for filtering the list of security incidents so you can quickly find the security incidents you want to analyze. The Quick Filters let you select a subset of the security incidents based on criteria in the filter.

![Quick filters](../image/quick-filters.png "Quick filters")

Simply click the quick filter you want to use.

**Note:** You can click an **Edit** button to identify which quick filters you want displayed on the list screen. A minimum of one filter must be selected, up to a maximum of six.

You can define additional quick filters, as well as primary filters for the Security Analyst Workspace, using the classic environment. For more information, see [Set up primary and secondary filters for Security Analyst Workspace](../task/set-up-filters-for-new-ui.md).

## Personalize the security incident list

As with all lists in your instance, the Security Analyst Workspace provides tools for personalizing the list and sorting the information displayed to meet your analysis needs.

![Security incident list filtering options](../image/si-filter-options.png "Personalize the security incident list")

## Save time with Peek view

Before opening a security incident record, you can save time using the Peek view. This feature allows you to quickly locate vital security artifacts without having to reload the entire page. Simply click the **&gt;** icon to the left of a security incident number to take a peek.

![Security incident showing the peek view](../image/peek-view.png "Peek view")

The peek view provides a snapshot of vital information in a single view. This view can save valuable time when you are working with multiple incidents. You can click the down arrows on certain fields to make on-the-fly updates, such as assigning an assignment group or a specific analyst.

![Peek details](../image/peek-details.png "Peek view details")

## Perform quick actions on a security incident

After you have selected and opened a specific security incident, you can perform time-saving actions on the record.

-   If you security incident is open, click the **Edit Record** icon to make quick changes to any of its fields. If the record is closed, you can change only its tag.
-   Click **Manage Attachments** to attach files to the security incident. You can also download or remove attached files and edit the encryption applied to the attachments.
-   Click **Compose Email** to send a quick email to a colleague. Emails can be free-form, or you can send canned emails selected from a list of templates. Emails sent and replies received are captured in the Incident Timeline.

    **Note:** You can create custom templates that contain reusable content for emails and email notifications. Variables can be used for inserting information specific to the security incident or alert, such as the subject line, priority, or threat category. Use the Security Incident \[sn\_si\_incident\] table for emails and email notifications related to Security Incident Response. For more information, see [Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

-   Click **More** to view a quick snapshot of the security incident, such as the description, business impact, and priority. You can also click the down-arrow in the **Assignment group** and **Assigned to** fields to make on-the-fly changes to those fields.

![Quick actions](../image/quick-actions.png "Assignment group")

## Work with multiple security incidents

The tabbed interface allows you to keep several security incidents open simultaneously so you can switch between them with a single click. This can save time and allow you to see the big picture when threats from multiple sources are identified.

![Security incident tabbed interface](../image/tabbed-interface.png "Work with multiple security incidents")

## View analysis information in the security incident tabs

When you open a security incident record, three tabs are shown:

-   Overview
-   Explore
-   Incident Timeline

## Overview tab

Use the **Overview** tab to view information in a security incident in a single location. No need to open another application or console.

![Overiew tab](../image/overview-tab.png "Overview")

The tiles that are displayed on the **Overview** tab are customizable. You can collapse and expand them as needed, and you can move them around by dragging the **Grip** icon. Click the **More options** icon to delete a tile or change its heading text.

![Getting around the Overview tab.](../image/work-notes-drag.png "Overview tab")

## Explore tab

Configure the tiles displayed on the **Overview** tab using the **Explore** tab. Simply select the tiles you want to view from the left-hand pane, and click the **Pin** icon. Pinned tiles automatically appear in the **Overview** tab.

![Pin to Overview](../image/pin-to-overview.png "Expore tab")

The left-hand pane of the **Explore** tab includes a wide variety of information that you can display on the **Overview** tab. For example, expand **Observables** to display these related lists.

-   Observables
-   Threat Lookup Results
-   Security Scan Results
-   Domain Lookups
-   Observable Enrichment

Additional related lists are available under **Users**, **Configuration Items**, and **Incidents**.

## Incident Timeline tab

Use the **Incident Timeline** tab during your investigation for tracking purposes. Every time an action is performed on a security incident, the system records it in the Incident Timeline.

-   You can also manually add worknotes to the timeline by typing them in the **Add work notes** box and clicking **Post**.
-   You can search for a specific timeline activity using the Search box.
-   The **Filter Activity** icon allows you to display only the types of timeline activity you want to see \(for example, only incidents created by a specific analyst\).
-   You can add or remove the Incident Timeline from the **Overview** tab using the **Pin/Unpin** icon.

![Incident Timeline](../image/incident-timeline-tab.png "Incident Timeline tab")

## Handle security incidents using the Playbook

Resolve certain types of security threats in a step-by-step manner using the built-in Security Analyst Playbooks. For example, an analyst can use the playbook to resolve phishing attacks and threats caused by malicious code activities. For more information, see [Resolve security threats with the playbook](../task/use-the-playbook.md#).

