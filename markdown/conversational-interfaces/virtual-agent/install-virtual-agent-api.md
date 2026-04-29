---
title: Install Virtual Agent API
description: Install the Virtual Agent API app to integrate any chat interface or a bot with ServiceNow Virtual Agent or Agent Chat.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Install Virtual Agent API

Install the Virtual Agent API app to integrate any chat interface or a bot with ServiceNow® Virtual Agent or Agent Chat.

## Before you begin

If you're upgrading from a version prior to version 2 and if authentication is required for your instance, you must revert the customization before upgrading. For these versions, the upgrade skips the Scripted REST Service when authentication is turned on. For more information, see [Revert a customization](https://www.servicenow.com/docs/access?context=uc-revert-customization&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

You must meet the following requirements:

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Virtual Agent API](https://store.servicenow.com/sn_appstore_store.do#!/store/application/62c44c6353311010ad77ddeeff7b120c/3.8.1?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%26q%3Dvirtual%2520agent%2520api&sl=sh) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Ensure that you activated the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin, which activates the Conversational Custom Chat Integration \(com.glide.cs.custom.adapter\) plugin.

    For more information about this plugin, see [Activate Virtual Agent](activate-virtual-agent.md).


**Note:** The Virtual Agent API requires a Pro license similar to that of Virtual Agent.

Role required: admin or virtual\_agent\_admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Virtual Agent API application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.


## What to do next

[Review the inbound REST endpoint and configure inbound authentication](configure-send-request.md)

**Parent Topic:**[Configuring Virtual Agent API](../concept/configure-virtual-agent-api.md)

