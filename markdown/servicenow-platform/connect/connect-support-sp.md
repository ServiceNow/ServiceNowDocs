---
title: Connect Support and Service Portal
description: Use Connect Support in your portal to allow your users to ask questions or submit requests to support agents. You configure the instance options to control the appearance of your widget and how it functions.You can control the appearance of your widget and how it functions by configuring the instance options.
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect Support, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Connect Support and Service Portal

Use Connect Support in your portal to allow your users to ask questions or submit requests to support agents. You configure the instance options to control the appearance of your widget and how it functions.

The Connect Support and Service Portal integration creates a Connect Support widget that you can add to a page in the Service Portal.

## Configure Connect Support widget instance options

You can control the appearance of your widget and how it functions by configuring the instance options.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration** and open the Service Portal Designer.

2.  From the Service Portal Designer, select the page you added the Connect Support widget to.

    If you have not yet added the widget to a page, see Create and edit a page using the Service Portal Designer for more information.

3.  Click the edit icon in the corner of the widget to open the instance options menu.

4.  Complete the fields using the following table.

    Depending on the functionality you want to add, you may not need to add all these fields.

    |Field|Description|
    |-----|-----------|
    |Bootstrap color|Select a color for your widget from a list of common bootstrap colors. Themes control the overall color of a widget, but if you want your widget to be a specific color, you can select it from the list.|
    |Queue URL|The URL for the Connect Support chat queue that you want questions to be directed to. For example, htts://&lt;instancename.service-now.com/$chat\_support.do?queueID=&lt;sys\_id&gt;|
    |Queue Name|The name of the queue you want the questions to be directed to. You can find a list of queue names in **Collaborate** &gt; **Connect Support** &gt; **Queues**.|
    |Queue ID|The sys\_id of the queue you want questions to be directed to. You can find this ID by going to the support queue and either copying the queue ID from the support link, or by selecting **Copy sys\_id** from the context menu.|
    |Message|The text for the button in the Connect Support widget|
    |Window|Use this option to open the chat in another tab rather than in a new window.|
    |Title|The name in the widget header|


