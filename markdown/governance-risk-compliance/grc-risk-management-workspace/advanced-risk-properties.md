---
title: Properties installed with Advanced Risk
description: Properties are added with activation of GRC: Advanced Risk. There are also properties that are available for the various capabilities such as risk events and advanced risk assessments.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Components installed with Advanced Risk, Reference, Risk Management, Governance, Risk, and Compliance]
---

# Properties installed with Advanced Risk

Properties are added with activation of GRC: Advanced Risk. There are also properties that are available for the various capabilities such as risk events and advanced risk assessments.

## Properties for Advanced Risk

All the properties for Advanced Risk, are listed on the System Properties page. To access the System Properties page, in the filter navigator, type **sys\_properties.list**.

<table id="table_xhk_4rk_ctb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum number of levels for risk hierarchy \[sn\_risk\_advanced.risk\_hierarchy\_max\_levels\]

</td><td>

Set the maximum number of levels of risk hierarchy.

 -   Type: Integer
-   Default value: 5

</td></tr><tr><td>

Configure risk rating \[sn\_risk\_advanced.risk\_rating\_config\]

</td><td>

Compare calculated risk score with either of choices Maximum calculated ALE, Minimum calculated ALE, Average calculated ALE. -   Type: choice list
-   Default value: avg

 **Note:** This property works with classic risk scoring.

</td></tr><tr><td>

Compare risk tolerance \[sn\_risk\_advanced.risk\_tolerance\]

</td><td>

Compare risk tolerance based on either of the choice Average, Maximum, Minimum, Sum.-   Type: choice list
-   Default value: sum

</td></tr><tr><td>

Enable the GRC enterprise risk licensing features \[sn\_risk\_advanced.enable\_irm\_advanced\_risk\_enterprise\]

</td><td>

This property enables the GRC enterprise risk licensing features.-   Type: true or false
-   Default value: false

</td></tr></tbody>
</table>## Properties for Risk Events

To access the risk event properties, navigate to **All** &gt; **Risk Events** &gt; **Administration** &gt; **Properties**.

<table id="table_dhr_rjk_3jb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Machine learning solution for predicting similar risk events \[ml\_sn\_sn\_grc\_pred\_intel\_global\_similar\_risk\_events\]

</td><td>

Solution definition for predicting similar risk events.

</td></tr><tr><td>

Show Basel attributes and reports \[sn\_risk\_advanced.show\_basel\_attr\_reports\]

</td><td>

Set this property to true if you want to enable the Basel categorization of risk events. This property is useful for customers in the banking domain. -   Type: True or false
-   Default value: false

</td></tr><tr><td>

Define risk event currency conversion configuration \[sn\_risk\_advanced.risk\_event\_currency\_conversion\_date\_config\]

</td><td>

Property to define currency conversion dates for the risk event entries. You can select specific dates for currency conversion rather than relying solely on the date of impact to calculate the net loss. The options are as follows:-   **Risk event entry date**
-   **First loss entry date**
-   **Last loss entry date**
-   **First recovery entry date**
-   **Last recovery entry date**
-   **Custom date**

**Note:** You can also override the defined currency conversion dates in the risk response template configuration. These changes apply to both new and ongoing risk event workflows.

</td></tr><tr><td>

Make risk event to risk relationship mandatory \[sn\_risk\_advanced.make\_riskevent\_to\_risk\_relation\_mandatory\]

</td><td>

Set this property to true if you want to ensure that each risk event has corresponding risks. -   Type: True or false
-   Default value: false

</td></tr><tr><td>

No. of days for Rapid Recovery Classification \[sn\_risk\_advanced.no\_of\_days\_for\_rapid\_recovery\_classification\]

</td><td>

Customize the number of days that users can set as their rapid recovery threshold.-   Type: Integer
-   Default value: 5

</td></tr><tr><td>

Show ORX External events \[sn\_risk\_advanced.show\_orx\_events\]

</td><td>

Users can choose to see the ORX External Events. ORX provides a platform for the secure exchange of high-quality operational risk loss data from around the world. This property is useful for customers in the banking domain.

 Customers import the ORX information as shared by the ORX organization. This information can be related to risk statement or control objectives. This information can be modified by users. -   Type: True or false
-   Default value: false

</td></tr><tr><td>

How many years of risk event data to be shown on the report \[sn\_risk\_advanced.number\_of\_years\_report\_data\]

</td><td>

Select how many years of risk event data must be shown on the report.

 -   Type: Integer
-   Default value: 2

 **Note:** This property is visible on the System Properties page.

</td></tr></tbody>
</table>## Properties for advanced risk assessment

To access the advanced risk assessment properties, navigate to **All** &gt; **Advanced Risk Assessments** &gt; **Administration** &gt; **Properties**.

<table id="table_mcl_y1k_ctb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Migrate to Advanced Risk Assessments \[sn\_risk\_advanced.hide\_risk\_legacy\_lifecycle\]

</td><td>

Migrate to Advanced Risk Assessments.-   Type: yes or no
-   Default value: no

</td></tr><tr><td>

Enable Advanced Risk PPM Integration \[sn\_risk\_advanced.enable\_advanced\_risk\_ppm\_integration\]

</td><td>

Perform project risk assessments. Only users with the it\_pps\_admin or sn\_ risk.admin roles can enable this property. -   Type: yes or no
-   Default value: no

 For more information, see [Configure Project Portfolio Management and Advanced Risk integration](../../grc-risk/task/specify-approvers-for-proj-risks.md) **Note:** This property is only available when Project Portfolio Management is installed.

</td></tr><tr><td>

sn\_risk\_advanced.metric\_approval

</td><td>

Enables Risk administrators to define either the simple approval flow or the advanced approval flow for all the metrics and metric definitions. **Note:** This property is available only when the sn\_grc\_appr plugin is activated and must be set while configuring the ESG Management application.

 The choices are as follows:-   **Simple**: By choosing this option, the Approval section will be enabled both on the manual metric definition form and within the metrics. Using this section, you can designate approvers directly on the metric definition form.
-   **Advanced**: When you choose this option, the Approval section will be unavailable on the manual metric definition form and the metric form. Instead, approval can be configured by setting the approval conditions, tables, and approvers in the GRC: Approver Configurator application. This application also allows you to define multiple levels of approvals. For more information see, [Using Approver Configurator for setting up approvals](../concept/approval-configuration.md).

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Advanced Risk](../../grc-risk/reference/components-risk-advanced.md)

