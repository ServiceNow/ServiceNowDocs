---
title: Create configuration values for risk scores
description: Use the Risk Score module to create configuration values for risk score bands.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/risk-score-config.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring risk, Configure, Enterprise Asset Management, Asset Management]
---

# Create configuration values for risk scores

Use the Risk Score module to create configuration values for risk score bands.

## Before you begin

Before creating configuration values for risk score, ensure that you have added and frozen configuration value for the two vectors: likelihood and impact in the Risk Likelihood and the Risk Impact modules, respectively.

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Admin center view.

3.  From the navigation panel of the Admin center view, navigate to **Risk configuration** &gt; **Risk score**.

4.  Select **New**.

5.  Fill in the form details.

<table id="choicetable_or4_fxl_stb"><thead><tr><th align="left" id="d172729e107">

Field

</th><th align="left" id="d172729e110">

Description

</th></tr></thead><tbody><tr><td id="d172729e116">

**Start**

</td><td>

Start value of the risk score band.

</td></tr><tr><td id="d172729e125">

**End**

</td><td>

End value of the risk score band. The value is automatically populated using the maximum likelihood and impact configuration values.

</td></tr><tr><td id="d172729e134">

**Label**

</td><td>

Label of the risk score band.

</td></tr><tr><td id="d172729e143">

**Color**

</td><td>

Color depicting a risk score band. Following are the values to choose from:-   Green
-   Yellow
-   Orange
-   Red


</td></tr></tbody>
</table>6.  Select **Submit**.

    Based on the other fields, the **Band name** field is automatically populated.

7.  To add more risk score bands, repeat steps 2-4.

    There should be a minimum of two score band records and a maximum of four.

8.  Select **Freeze** after you have added the entire risk range.

    To edit the records, select **Unfreeze**.


**Parent Topic:**[Managing risk in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/managing-eam-risk-scores.md)

