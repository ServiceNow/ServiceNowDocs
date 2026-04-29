---
title: Enable or disable global header options
description: Enable or disable the global header options by configuring additional options in JSON format for the Employee Center menu record.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Employee Center global header, Admin configurations, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Enable or disable global header options

Enable or disable the global header options by configuring additional options in JSON format for the Employee Center menu record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Portals** &gt; **Portals**.

    The Service Portal module displays the list of all the available portals.

2.  Click **Employee Center**.

    If the Employee Center form is read-only, the message `To edit this record click here` appears at the top.

3.  Click **here** to edit the form.

4.  Beside the **main menu** field, click the **Preview this record** icon to open the Employee Center menu record.

5.  Edit the **Additional options, JSON format** field.

<table id="choicetable_osb_gxg_5qb"><thead><tr><th align="left" id="d438894e113">

Option

</th><th align="left" id="d438894e116">

Parameter setting

</th></tr></thead><tbody><tr><td id="d438894e122">

**Search bar**

</td><td>

To enable this option, set the `exclude_search_on_homepage` value to **false**.```
"exclude_search_on_homepage":{
		"displayValue":"false",
		"value":false
```

Default value: true**Note:** By default, the search widget is displayed in the Employee Center homepage. Search bar on the global header is hidden by default that you can enable, if needed.

</td></tr><tr><td id="d438894e146">

**Wishlist**

</td><td>

To enable this option, set the `enable_wishlist` value to **true** ```
"enable_wishlist":{
		"displayValue":"true",
		"value":true
```

Default value: False

</td></tr><tr><td id="d438894e164">

**My Requests**

</td><td>

To disable this option, set the `enable_requests` value to **false** ```
"enable_requests":{
		"displayValue":"false",
		"value":false
```

Default value: True

</td></tr><tr><td id="d438894e182">

**My Tasks**

</td><td>

To disable this option, set the `enable_tasks` value to **false** ```
"enable_tasks":{
		"displayValue":"false",
		"value":false
```

Default value: True

</td></tr><tr><td id="d438894e201">

**More**

</td><td>

To disable this option, set the `enable_more_items` value to **false** ```
"enable_more_items":{
      	"displayValue":"false",
      	"value":true,
"sysId":"47c952cbec8305107f44e04d648d43c0"

```

Default value: True

</td></tr><tr><td id="d438894e219">

**Cart**

</td><td>

To enable this option, set the `enable_cart` value to **true** ```
"enable_cart":{
		"displayValue":"true",
		"value":true
```

Default value: False

</td></tr><tr><td id="d438894e237">

**Update Cart**

</td><td>

To enable this option, set the `auto_update_cart` value to **true**. Update the shopping cart automatically with user-specific changes from multiple tabs and platforms.```
"auto_update_cart": {
        "displayValue": "true",
          "value": true}
```

Default value: True

</td></tr></tbody>
</table>    **Note:** For a topic to show up in the **Header Menu**, ensure that you add content to the topic.

6.  Click **Update**.


