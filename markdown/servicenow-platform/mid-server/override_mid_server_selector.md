---
title: Override the MID Server selection filter
description: Use the override feature to write your own filter condition that overrides the normal MID Server selection criteria for an application. An override has precedence over the default filter and can be defined for a specific selection condition.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [MID Server selection, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Override the MID Server selection filter

Use the override feature to write your own filter condition that overrides the normal MID Server selection criteria for an application. An override has precedence over the default filter and can be defined for a specific selection condition.

## Before you begin

Before attempting to create an override filter, be sure you understand the criteria the platform uses to select MID Servers. See [MID Server selection](../concept/c_MIDServerSelector.md) for details.

Role required: admin

<table id="table_irs_ps4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>## About this task

**Note:** The override feature is intended for Cloud Management and Cloud Discovery only. The **Override by capability** filter is provided by default.

There are four MID Server selection filters included in the base ServiceNow system. These filters are applied to all MID Servers in order until the system finds a matching condition:

-   Status Filter
-   App Filter
-   Capability Filter
-   IP Filter

**Important:** The override feature allows multiple filter types but only one override filter for each filter type. The **Override selector** filter type overrides all other filters and takes complete control of the MID Server selection. If this type is active, it is the only filter applied.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Mid Selector Override**.

    The list of MID Server overrides appears.

2.  Select **New** to create a new filter.

3.  Complete these fields:

    -   **Name**: Unique name for this override. Ensure that you can identify the override type by the name.
    -   **Script**: Condition for this filter. Create the MID Server selection logic for your override in this field, using the directions provided in the function template. Look at the **Override by capability** filter as an example before starting to create your filter.
    -   **Type**: Type of override being configured. Select one of the four default filters to override with your condition, or select **Override selector** to create a filter that overrides all the others.
4.  Select **Submit**.

    ![MID Server override filter script](../image/MIDSelectionOverride.png)


## Example

The Cloud Discovery schedule selects MID Servers based on Applications and Capabilities. To select different MID Servers for different service accounts, you can customize the **MID Selector Override**. After the line `(function filter(/* MIDServerJS Array */ candidateMIDList, /* MIDServerJS Array */ defaultSelectedMIDList, /* Native JS object */ midSelectorContext, /* MIDSelectorParamJS */ requestedParameters) {` add the following code with your information:

```
var result = [];

 if (JSON.parse(midSelectorContext).service_account_id == '[example-account-id]') {
  for (var mid in defaultSelectedMIDList) {
   if (defaultSelectedMIDList[mid].sysId == '[example-MID-1]' || defaultSelectedMIDList[mid].sysId == '[example-MID-2]')
    result.push(defaultSelectedMIDList[mid]);
  }
  return result;   
 }
```

**Parent Topic:**[MID Server selection](../concept/c_MIDServerSelector.md)

