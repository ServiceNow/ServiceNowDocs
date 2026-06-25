---
title: Make a Connect Support queue accessible to end users
description: To make a Connect Support queue accessible to end users, use the accepted URL format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/connect/t\_MakeConnectSupportQueueAccessible.html
release: australia
product: Connect
classification: connect
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect Support administration, Connect Support, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Make a Connect Support queue accessible to end users

To make a Connect Support queue accessible to end users, use the accepted URL format.

## Before you begin

Create a queue. Create agents for the queue by assigning users to the assignment group associated with the queue.

Role required: admin

## About this task

For example, you might create a module or add a link to a portal. The accepted URL format is `https://<instancename>.service-now.com/$chat_support.do?queueID=<sys_id>`.

## Procedure

1.  Navigate to **All** &gt; **Connect** &gt; **Administration** &gt; **Queues**.

2.  Right-click the name of the queue to which you want to link.

3.  In the context menu, select **Copy sys\_id**.

4.  Follow browser instructions to copy the sys\_id if browser security measures restrict this function.

5.  Preview the support queue by navigating to `https://<instancename>.service-now.com/$chat_support.do?queueID=<sys_id>`.

6.  Create a module or other link to the queue using the URL.


**Related topics**  


[Create a module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/test-steps-app-navigator-category.md)

[Configure Connect Support widget instance options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/connect/connect-support-sp.md)

