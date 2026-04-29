---
title: Configure which external apps are available for deep linking
description: Administrators can define which external apps can be used in deep links with the glide.sg.allowed\_external\_deeplinks property.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure which external apps are available for deep linking

Administrators can define which external apps can be used in deep links with the **glide.sg.allowed\_external\_deeplinks** property.

## Before you begin

Role required: admin

## About this task

ServiceNow mobile supports deep linking to third-party applications using the **URL** smart buttons. Use the **glide.sg.allowed\_external\_deeplinks** system property to define which third-party applications can be used as the targets of deep links in your ServiceNow mobile apps.

**Important:** Only custom URL schemes are supported. App links and universal links are not supported.

## Procedure

1.  Type `sys_properties.list` in the Application Navigator.

2.  Open the record for **glide.sg.allowed\_external\_deeplinks**.

3.  In the form, match the following values:

<table id="table_tgg_45x_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.sg.allowed\_external\_deeplinks**

</td></tr><tr><td>

Type

</td><td>

String

</td></tr><tr><td>

Value

</td><td>

Comma-separated list of the names of the third-party apps that can be targets of deep links within ServiceNow mobile apps.

 For example: `Teams, LinkedIn, Zoom`

</td></tr></tbody>
</table>4.  Click **Save**.


## Result

Only third-party apps listed in value of the property can be linked to using deep linking.

**Note:** If the value of this property is left empty, or the property is deleted, there are no restrictions on deep linking to third-party apps.

**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)

