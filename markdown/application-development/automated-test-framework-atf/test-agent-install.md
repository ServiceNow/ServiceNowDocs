---
title: Install ATF troubleshooting agent
description: Install the ServiceNow Otto for Creator application from the ServiceNow Store to get the ATF troubleshooting agent application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/test-agent-install.html
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ATF troubleshooting agent, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Install ATF troubleshooting agent

Install the ServiceNow Otto for Creator application from the ServiceNow Store to get the ATF troubleshooting agent application.

## Before you begin

-   Review the [ServiceNow Otto for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   The default model provider for ATF troubleshooting agent is Anthropic Claude on AWS.

Ensure that the following applications are installed:

-   Build Agent: See [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/install-build-agent.md) for more information.
-   ATF Test Generator and Cloud Runner: Install the [ATF Test Generator and Cloud Runner](https://store.servicenow.com/store/app/e4292f6e1be06a50a85b16db234bcbc3) store application from ServiceNow store. You also need to set up the cloud user for seamless execution from the Build Agent interface. See [ATF Test Generator and Cloud Runner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/atf-tg-cr-intro.md) and [Set up cloud user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/atf-tg-cr-configure.md) for more information.

Role required: admin

## Procedure

1.  From the ServiceNow Otto for Creator application page on the ServiceNow Store, select **Buy**.

2.  After approval has been granted, on your instance, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Using the search bar, search for the ServiceNow Otto for Creator application \(sn\_now\_creator\).

4.  Select **Install**.

5.  Enable the ATF troubleshooting agent skill:

    1.  Navigate to **Admin** &gt; **AI Admin Hub**.

    2.  Go to the **Now Assist Skills** tab and select **Creator**.\[Omitted image "atf-troubleshooting-agent.png"\] Alt text: ATF troubleshooting agent is listed as Now Assist for Creator skills.

    3.  Select **Turn on** to enable the skill.

    The skill is enabled for all users.


