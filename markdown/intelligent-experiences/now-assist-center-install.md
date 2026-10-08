---
title: Confirm installation of AI Admin Center
description: Confirm the installation of the AI Admin Center application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-center-install.html
release: brazil
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Configure, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Confirm installation of AI Admin Center

Confirm the installation of the AI Admin Center application.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Review the [AI Admin Center](https://store.servicenow.com/store/app/6c298ff8c3b932546a2eb043e40131ba) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

AI Admin Center installs and runs automatically as part of the standard ServiceNow Otto for Platform setup. No manual steps are required. After ServiceNow Otto panel for Platform is installed and configured, AI Admin Center will be present on your instance.

Follow these steps to confirm the installation of the AI Admin Center plugin.

## Procedure

1.  Confirm the AI Admin Center plugin is installed by navigating to **All** &gt; **System Definition** &gt; **Plugins** and selecting the **Installed** tab.

2.  If the AI Admin Center plugin is not installed, perform the following steps to manually install it.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

    2.  In the search box, type `AI Admin Center`.

    3.  In the Store applications section under the Available for you tab, select the **AI Admin Center** card.

    4.  Select **Install**.

    5.  Select a version from the list.

    6.  Review the installation details and select **Continue**.

    7.  Select an installation schedule option.

    8.  Select **Install**.

        The AI Admin Center application will install at the selected time.

3.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center** to confirm the successful installation.


## Result

The application is installed and available to the appropriate user roles.

**Parent Topic:**[Configuring AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configuring-now-assist-center.md)

**Related topics**  


[Enable the ServiceNow Otto panel \(Next Experience UI\)]()

[Enable the ServiceNow Otto panel \(Lux UI\)]()

