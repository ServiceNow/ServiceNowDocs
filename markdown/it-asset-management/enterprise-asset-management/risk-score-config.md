---
title: Create configuration values for risk scores
description: Use the Risk Score module to create configuration values for risk score bands.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/risk-score-config.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring risk, Configure, Enterprise Asset Management, IT Asset Management]
---

# Create configuration values for risk scores

Use the Risk Score module to create configuration values for risk score bands.

## Before you begin

Before creating configuration values for risk score, ensure that you have added and frozen configuration value for the two vectors: likelihood and impact in the Risk Likelihood and the Risk Impact modules, respectively.

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Admin center** &gt; **Risk configuration** &gt; **Risk score**.

2.  Select **New**.

3.  Fill in the form details.

<table id="choicetable_or4_fxl_stb"><thead><tr><th align="left" id="d76146e89">

Field

</th><th align="left" id="d76146e92">

Description

</th></tr></thead><tbody><tr><td id="d76146e98">

**Start**

</td><td>

Start value of the risk score band.

</td></tr><tr><td id="d76146e107">

**End**

</td><td>

End value of the risk score band. The value is automatically populated using the maximum likelihood and impact configuration values.

</td></tr><tr><td id="d76146e116">

**Label**

</td><td>

Label of the risk score band.

</td></tr><tr><td id="d76146e125">

**Color**

</td><td>

Color depicting a risk score band. Following are the values to choose from:-   Green
-   Yellow
-   Orange
-   Red


</td></tr></tbody>
</table>4.  Select **Submit**.

    Based on the other fields, the **Band name** field is automatically populated.

5.  To add more risk score bands, repeat steps 2-4.

    There should be a minimum of two score band records and a maximum of four.

6.  Select **Freeze** after you have added the entire risk range.

    To edit the records, select **Unfreeze**.


**Parent Topic:**[Managing risks scores in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/managing-eam-risk-scores.md)

