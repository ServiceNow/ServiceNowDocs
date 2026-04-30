---
title: User guide help URLs
description: You can create entry points in your instance for help generated with the system user guide by providing the correct address parameters in the target URL.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [System user guide, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# User guide help URLs

You can create entry points in your instance for help generated with the system user guide by providing the correct address parameters in the target URL.

Help pages generated with the user guide can be displayed to end users from configurable entry points in the system, including [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). To create these entry points, you must express a target URL using these parameters:

|Parameter|Provides|
|---------|--------|
|$h.do|Processor that renders the banner frame at the top of the page.|
|$sys\_product\_help.do|Displays a page containing links to all the help in the user guide. This includes the basic help system and any custom help pages you have created. An example URL would be `https://myinstance.service-now.com/$sys_product_help.do`.|
|$h.do?sysparm\_id=basics|Displays the basic help page included with the system. To create a target for a custom user guide, replace **id=basic** with the ID for your custom page, such as **id=surveys**. An example of this would be `https://myinstance.service-now.com/$h.do?sysparm_id=surveys`.|
|$h.do?sysparm\_doc=&lt;document number&gt;|Displays help for a specific document. This URL displays the help document in the basic page that provides instructions for using ServiceNow forms: `https://myinstance.service-now.com/$h.do?sysparm_doc=DOC0010005`.|

**Parent Topic:**[System user guide](../concept/c_SystemUserGuide.md)

