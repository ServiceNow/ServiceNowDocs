---
title: Install ServiceNow Otto for RPA Hub
description: If you have the admin role, you can install the ServiceNow Otto for RPA Hub application so that your human agents or users can get started with developing automations faster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/configure-now-assist-rpa-hub.html
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Configure, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Install ServiceNow Otto for RPA Hub

If you have the admin role, you can install the ServiceNow Otto for RPA Hub application so that your human agents or users can get started with developing automations faster.

## Before you begin

-   Review the ServiceNow Otto for RPA Hub application listing in ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Perform these steps in your ServiceNow instance.
-   Ensure that the AI Search application is enabled on your instance by navigating to **All** &gt; **AI Search** &gt; **AI Search Status**. If AI search is not enabled, select **Request AI Search**.
-   Role required: admin

## About this task

**Important:** The ServiceNow Otto for RPA Hub requires a separate subscription to ServiceNow Otto for Creator.

## Procedure

1.  Perform any of the following tasks to install the ServiceNow Otto for RPA Hub application.

<table id="choicetable_b2q_dpq_y2c"><thead><tr><th align="left" id="d103055e123">

Option

</th><th align="left" id="d103055e126">

Action

</th></tr></thead><tbody><tr><td id="d103055e132">

**From AI Admin Hub**

</td><td>

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Settings** &gt; **Plugins**.
2.  On the **Available for you** tab, select **ServiceNow Otto for RPA Hub**.
3.  Select **Get plugins**.
4.  In the Install ServiceNow Otto for RPA Hub plugins, select **Install Plugin**.
5.  Select **Install**.


</td></tr><tr><td id="d103055e196">

**From System Applications**

</td><td>

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.
2.  Find the ServiceNow Otto for RPA Hub application \(sn\_rpa\_na\) using the filter criteria and search bar.

You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

In the Install dialog box that is displayed, any dependencies that are installed along with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.
5.  Select **Install**.


</td></tr></tbody>
</table>
## Result

To view the installed plugins, navigate to **All** &gt; **AI Admin Hub** &gt; **Settings** &gt; **Plugins**. You can view ServiceNow Otto for RPA Hub in the Installed tab.\[Omitted image "installed-narh-plugin.png"\] Alt text: Plugins tab that displays the ServiceNow Otto for RPA Hub as installed.

## What to do next

If you're upgrading to the Yokohama Patch 3 release, reindex the data source. For more information, see [Perform a full table index or reindex for multiple AI Search indexed sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/index-multiple-sources-ais.md). In the step 2 of this procedure, select the indexed source as RPA Component \[sn\_rpa\_na\_rpa\_component\].

Turn on the Robotic Process Automation \(RPA\) bot generation skill to use generative AI to create automations, activities, and automation logic additions from text instructions and preview options. For more information, see [Turn on the RPA bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/turn-rpa-bot-generation-skill.md).

