---
title: Components installed with Continuous Authorization and Monitoring
description: Activating the GRC: CAM plugin adds or modifies several tables, user roles, and other components.Default properties are set with activation of CAM plug-in.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CAM reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Components installed with Continuous Authorization and Monitoring

Activating the GRC: CAM plugin adds or modifies several tables, user roles, and other components.

**Parent Topic:**[CAM reference](../concept/reference-grc-cam.md)

## Continuous Authorization and Monitoring system properties

Default properties are set with activation of CAM plug-in.

To configure the CAM report properties, navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **System Properties**.

-   Enter the days in the **Days before Next Authorization to create engagement** field to automatically create the next engagement in the authorization package. The days entered in this field in System Properties are subtracted from the next authorization date to determine the next engagement date, which is recorded in the authorization package.

    For more information, see [View package details in CAM Workspace](../../grc-cam-workspace/task/auth-package-overview-ws.md).

-   In the **Homepage Title** field, you can customize the homepage title. Enter your organization-specific terminology. The default value is Continuous Authorization Monitoring. The homepage title updates immediately after saving.
-   In the **Days Before Next Authorization** field, you can configure authorization timing. Enter the number of days before reauthorization that the system should display a warning.

![ATO Artifacts System Properties.](../../grc-cam-workspace/image/cam-ato-artifacts-system-properties.png)

<table id="table_wxn_rh3_ydc"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Options

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

sn\_irm\_cont\_auth.sn\_irm\_cont\_auth\_ssp\_report\_type

</td><td>

Specifies the type of template to be used for System Security Plan \(SSP\) report. By default, the HTML template is applied, but it can be configured to use a Word template based on customer requirements.

</td><td>

-   HTML template \(Default\)
-   Word template

</td><td>

-   HTML: 9cd38d7077b60210762c12738f5a9977
-   Word: 5b755a8447b15610ce3ab9b4416d43e0

</td></tr><tr><td>

sn\_irm\_cont\_auth.sn\_irm\_cont\_auth\_sar\_report\_type

</td><td>

Specifies the type of template to be used for SAR reports. By default, the HTML template is applied, but it can be configured to use a Word template based on customer requirements.

</td><td>

-   HTML template \(Default\)
-   Word template

</td><td>

-   HTML: 58b4749077a60210762c12738f5a99a6
-   Word: e30fe8792b9d1610d3b7fb466e91bf56

</td></tr><tr><td>

sn\_irm\_cont\_auth.sn\_irm\_cont\_auth\_poam\_report\_type

</td><td>

Specifies the type of template to be used for Plan of Actions and Milestones \(POA&amp;Ms\) report. By default, the HTML template is applied, but it can be configured to use a Word template based on customer requirements.

</td><td>

-   HTML template \(Default\)
-   Word template

</td><td>

-   HTML: 40a881663b2206108ce4d22c95e45aae
-   Word: 23b783892b8d1610d3b7fb466e91bfcf

</td></tr><tr><td>

sn\_irm\_cont\_auth.sn\_irm\_cont\_auth\_sap\_report\_type

</td><td>

Specifies the type of template to be used for SAP report. By default, the Word template is applied, but it can be configured to use an HTML template based on customer requirements.

</td><td>

-   HTML template
-   Word template \(Default\)

</td><td>

-   HTML: NA
-   Word: 9f41f3564786d610ce3ab9b4416d431b

</td></tr><tr><td>

sn\_irm\_cont\_auth.sn\_irm\_cont\_auth\_ato\_letter\_report\_type

</td><td>

Specifies the type of template to be used for Authority to Operate \(ATO Letter\) report. By default, the Word template is applied, but it can be configured to use an HTML template based on customer requirements.

</td><td>

-   HTML template
-   Word template \(Default\)

</td><td>

-   HTML: NA
-   Word: a673d03147f91e10ce3ab9b4416d4306

</td></tr><tr><td>

sn\_irm\_cont\_auth.sn\_irm\_cont\_auth\_executive\_summary\_report\_type

</td><td>

Specifies the type of template to be used for Executive Summary report. By default, the Word template is applied, but it can be configured to use an HTML template based on customer requirements.

</td><td>

-   HTML template
-   Word template \(Default\)

</td><td>

-   HTML: NA
-   Word: a533486e47711250ce3ab9b4416d4303

</td></tr></tbody>
</table>