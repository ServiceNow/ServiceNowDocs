---
title: Set up mappings between themes
description: Make sure that playbooks run as expected in your Service Portal by setting up mappings between your Service Portal theme and the UXF theme used in UI Builder.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Playbooks in Service Portal, Designing playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Set up mappings between themes

Make sure that playbooks run as expected in your Service Portal by setting up mappings between your Service Portal theme and the UXF theme used in UI Builder.

## Before you begin

Role required: admin, or portal admin with either snc\_internal or snc\_external

## About this task

The Portal Playbook widget uses a system property **ux\_portal\_theme\_to\_uib\_theme\_mapping** to handle mappings between a Portal page theme and a UXF theme​.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Select **New** in the upper right corner.

3.  Enter values for the following fields.

<table id="choicetable_aw3_gbw_ybc"><thead><tr><th align="left" id="d64143e99">

Field

</th><th align="left" id="d64143e102">

Description

</th></tr></thead><tbody><tr><td id="d64143e108">

**Name**

</td><td>

Specify your Service Portal property in the name. Give your system property the name **ux\_portal\_theme\_to\_uib\_theme\_mapping.\[the sys ID of your service portal theme\]**. For example, if you use the La Jolla theme for your Service Portal, it has a sys ID of a7a6e78277002300a6e592718a10617a​. You would enter **ux\_portal\_theme\_to\_uib\_theme\_mapping.a7a6e78277002300a6e592718a10617a​** as the name.​

</td></tr><tr><td id="d64143e129">

**Value**

</td><td>

To specify the sys UX theme and sys UX style that you want to map the Service Portal theme to, enter a comma-separated string of **\[the sys ID for the sys UX theme\], \[the sys ID of the sys UX style\]**. For example, if you want to map your Service Portal theme to the Polaris UX theme in dark mode, the sysId for the Polaris UX theme is 31bf91ae07203010e03948f78ad30095, and sys ID for the Dark sys UX style is e09ef7ae07103010e03948f78ad3002c. You would enter **31bf91ae07203010e03948f78ad30095, e09ef7ae07103010e03948f78ad3002c** as the value.​**Note:** The second value in this string is always an optional sys\_ux\_style. The first value is always the sys\_ux\_theme.

</td></tr></tbody>
</table>4.  In the form context menu, select **Save**.


## Result

The mapping between your Service Portal theme and the UXF theme is saved. Launch the playbook in Service Portal to see your changes.

**Note:** To turn a mapping off, you must delete it.

## What to do next

Embed a playbook in a Service Portal page and customize the Service Portal playbook runtime experience in the ServiceNow AI Platform®.

To learn more about customizing the playbook runtime experience in Service Portal, see [Embed the playbook in Service Portal](embed-playbook-service-portal.md).

**Parent Topic:**[Playbooks in Service Portal](../concept/playbooks-service-portal.md)

