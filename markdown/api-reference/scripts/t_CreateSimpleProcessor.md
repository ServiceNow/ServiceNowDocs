---
title: Create a simple processor
description: Create a simple processor to execute a script from a URL query. This feature is deprecated.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Processors, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Create a simple processor

Create a simple processor to execute a script from a URL query. This feature is deprecated.

## Before you begin

You must have your own demonstration instance.

Role required: admin

## About this task

**Note:** This feature is deprecated. While legacy, existing custom processors continue to be supported, creating new custom processors has been deprecated. Instead, use the [Scripted REST APIs](../../../../integrate/custom-web-services/concept/c_CustomWebServices.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Processors**.

2.  Select **New**.

3.  Enter the following information.

<table id="choicetable_wfd_v4x_3q"><thead><tr><th align="left" id="d512998e106">

Field

</th><th align="left" id="d512998e109">

Value

</th></tr></thead><tbody><tr><td id="d512998e115">

**Name**

</td><td>

Hello

</td></tr><tr><td id="d512998e124">

**Type**

</td><td>

Script

</td></tr><tr><td id="d512998e133">

**Path**

</td><td>

Hello

</td></tr><tr><td id="d512998e142">

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


**Parent Topic:**[Processors](../../../../script/processors/concept/c_Processors.md)

