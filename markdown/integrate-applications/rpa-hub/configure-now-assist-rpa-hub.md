---
title: Configure Now Assist for RPA Hub
description: If you have the admin role, you can configure the Now Assist for RPA Hub application so that your human agents or users can get started with developing automations faster.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist for RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Configure Now Assist for RPA Hub

If you have the admin role, you can configure the Now Assist for RPA Hub application so that your human agents or users can get started with developing automations faster.

## Before you begin

-   Review the Now Assist for RPA Hub application listing in ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Perform these steps in your ServiceNow instance.
-   Role required: admin

## About this task

**Important:** The Now Assist for RPA Hub requires a separate subscription to Now Assist for Creator.

Refer to the [Now Assist Overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/sn-assist-overview.pdf) to see the prebuilt skills that exist and are currently available for purchase in ServiceNow Now Assist packages and to review the number of assists consumed.

## Procedure

1.  Perform any of the following tasks to install the Now Assist for RPA Hub application.

<table id="choicetable_b2q_dpq_y2c"><thead><tr><th align="left" id="d108156e113">

Option

</th><th align="left" id="d108156e116">

Action

</th></tr></thead><tbody><tr><td id="d108156e122">

**From Now Assist Admin**

</td><td>

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings** &gt; **Plugins**.
2.  On the **Available for you** tab, select **Now Assist for RPA Hub**.
3.  Select **Get plugins**.
4.  In the Install Now Assist for RPA Hub plugins, select **Install Plugin**.
5.  Select **Install**.


</td></tr><tr><td id="d108156e184">

**From System Applications**

</td><td>

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.
2.  Find the Now Assist for RPA Hub application \(sn\_rpa\_na\) using the filter criteria and search bar.

You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

In the Install dialog box that is displayed, any dependencies that are installed along with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.
5.  Select **Install**.


</td></tr></tbody>
</table>
## Result

To view the installed plugins, navigate to **All** &gt; **Now Assist Admin** &gt; **Settings** &gt; **Plugins**. You can view Now Assist for RPA Hub in the Installed tab.![Plugins tab that displays the Now Assist for RPA Hub as installed.](../image/installed-narh-plugin.png)

## What to do next

If you are upgrading to the Yokohama Patch 3 release, reindex the data source. For more information, see [Perform a full table index or reindex for multiple AI Search indexed sources](https://www.servicenow.com/docs/access?context=index-multiple-sources-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). In the step 2 of this procedure, select the indexed source as RPA Component \[sn\_rpa\_na\_rpa\_component\].

Turn on the Robotic Process Automation \(RPA\) bot generation skill to use generative AI to create automations, activities, and automation logic additions from text instructions and preview options. For more information, see [Turn on the RPA bot generation skill](turn-rpa-bot-generation-skill.md).

