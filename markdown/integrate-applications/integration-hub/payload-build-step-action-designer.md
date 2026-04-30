---
title: Payload Builder step
description: Enable action designers to easily create name-value pairs in JSON and XML payloads using dynamic data.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration steps, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Payload Builder step

Enable action designers to easily create name-value pairs in JSON and XML payloads using dynamic data.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

**Note:** For JSON, this step is deprecated and replaced by the [JSON Builder step](json-build-step-action-designer.md).

## Fields

<table id="table_hqc_ckq_2fb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name Value Pairs

</td><td>

The name-value pairs to include in the payload. Click the plus icon to add name-value pairs. Drag data pills into either field to produce dynamic payloads.

 The **Name** becomes a key in JSON and an element in XML. For example, suppose you create this name-value pair.

-   **Name**: `short_description`
-   **Value**: `[action]->[short_description]`

 When the system formats the name-value pair as JSON:

```
"short_description": "[action]->[short_description]"
```

 When the system formats the name-value pair as XML:

 ```
<short_description>[action]->[short_description]</short_description>
```

</td></tr><tr><td>

Omit if empty

</td><td>

The option to exclude a name-value pair if the value is empty or null.**Note:** This field is only visible after clicking the down arrow to display advanced options.

</td></tr><tr><td>

Output Format

</td><td>

The payload file format.-   **JSON**: Select to format the payload as a JSON document.
-   **XML**: Select to format the payload as an XML document.

</td></tr><tr><td>

Namespace

</td><td>

The XML namespace to apply to each element. For example, when the namespace is set to `incident`:```
<incident:short_description>[action]->[short_description]</incident:short_description>
```

 **Note:** This field is only visible when the **Output Format** is set to **XML**.

</td></tr><tr><td>

Include Outer Structure

</td><td>

The option to include or exclude a top level container appropriate to the output format. When the **Output Format** is JSON, curly braces contain the name-value pairs. When the **Output Format** is XML, a specified XML element contains the name-value pairs.

 For example, when the system formats the name-value pair as JSON:

 ```
{
  "short_description": "[action]->[short_description]"
}
```

 When the system formats the name-value pair as XML:

 ```
<xml>
  <short_description>[action]->[short_description]</short_description>
</xml>
```

</td></tr><tr><td>

Send Empty Structure

</td><td>

The option to send valid JSON or XML structures when the payload is empty. Enable this option to include JSON or XML structural text in the payload.

 For example, when the system formats an empty structure as JSON:

```
{}
```

 When the system formats an empty structure as XML:

 ```
<xml></xml>
```

 Disable this option to produce an empty payload.

 Empty payloads can occur when you select the **Omit if empty** option for every name-value pair, and all name-value pairs in the payload produce empty values.

</td></tr><tr><td>

Parent Node

</td><td>

The name of the XML element that contains the name-value pairs. The default parent node element is `xml`.**Note:** This field is only visible when the **Output Format** is set to **XML** and the option to **Include Outer Structure** is enabled.

</td></tr><tr><td>

Preview

</td><td>

The read-only payload the step produces.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](https://www.servicenow.com/docs/access?context=action-error-evaluation&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


