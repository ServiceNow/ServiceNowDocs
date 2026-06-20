---
title: Create a simple processor
description: Create a simple processor to execute a script from a URL query. This feature is deprecated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/scripts/t\_CreateSimpleProcessor.html
release: xanadu
product: Scripts
classification: scripts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Processors, Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Create a simple processor

Create a simple processor to execute a script from a URL query. This feature is deprecated.

## Before you begin

You must have your own demonstration instance.

Role required: admin

## About this task

**Note:** This feature is deprecated. While legacy, existing custom processors continue to be supported, creating new custom processors has been deprecated. Instead, use the .

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Processors**.

2.  Select **New**.

3.  Enter the following information.

<table id="choicetable_wfd_v4x_3q"><thead><tr><th align="left" id="d193395e102">

Field

</th><th align="left" id="d193395e105">

Value

</th></tr></thead><tbody><tr><td id="d193395e111">

**Name**

</td><td>

Hello

</td></tr><tr><td id="d193395e120">

**Type**

</td><td>

Script

</td></tr><tr><td id="d193395e129">

**Path**

</td><td>

Hello

</td></tr><tr><td id="d193395e138">

**Script**

</td><td>

```
var name= g_request.getParameter("name");
g_processor.writeOutput("text/plain","Hello "+name);
```

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Enter a URL query to the instance with the following format: `https://instance.service-now.com/processor_name.do?parameter=value`

    For example: `https://<instancename>.service-now.com/Hello.do?name=world`.


**Parent Topic:**[Processors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/scripts/c_Processors.md)

