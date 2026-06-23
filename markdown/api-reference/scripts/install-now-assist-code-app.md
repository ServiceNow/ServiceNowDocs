---
title: Install Now Assist for code generation
description: Install the ServiceNow Now Assist for Creator application from the ServiceNow Store to get Now Assist for code generation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/api-reference/scripts/install-now-assist-code-app.html
release: xanadu
product: Scripts
classification: scripts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring code generation, Now Assist for code generation, Scripting, API implementation, API implementation and reference]
---

# Install Now Assist for code generation

Install the ServiceNow® Now Assist for Creator application from the ServiceNow® Store to get Now Assist for code generation.

## Before you begin

-   Review the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility. Now Assist for Creator installs the Now Assist for code generation application \(sn\_now\_assist\_code\).

Role required: admin

## Procedure

1.  From the Now Assist for Creator application page on the ServiceNow Store, select **Request App**.

2.  After approval has been granted, on your instance, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Using the search bar, search for the Now Assist for Creator application \(sn\_now\_creator\).

4.  Select **Install**.

5.  Verify that Now Assist for Creator is installed:

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features**.

    2.  In the workflow list, select **Creator**.

    3.  On the Code Assist card, verify that the code generation skill is active.

        \[Omitted image "now-assist-code-skill.png"\] Alt text: Code assist card displaying the Text-to-code skill in Now Assist Admin.

    For more information about Now Assist Admin, see [Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/platform-now-assist-landing.md).


## What to do next

Grant the now.assist.creator role to each user you want to use code generation.

**Parent Topic:**[Configuring code generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/scripts/configuring-now-assist-code.md)

**Related topics**  


[Install Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/build-workflows/now-assist-for-creator/install-now-assist-for-creator.md)

