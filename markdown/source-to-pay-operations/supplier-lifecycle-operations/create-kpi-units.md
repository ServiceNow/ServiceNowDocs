---
title: Create KPI units
description: Create KPI units to be used as measurement units for the quantitative performance of the supplier KPIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/create-kpi-units.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Supplier Relationship and Performance Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create KPI units

Create KPI units to be used as measurement units for the quantitative performance of the supplier KPIs.

\[Omitted video\] Description: Creating KPI Units.

## Before you begin

Role required: sn\_kpi.admin or sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Navigate to **All**.

2.  In the navigation filter, enter `sn_kpi_unit.LIST`.

    The list of existing units are displayed.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_u4m_243_btb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Indicates whether the KPI unit record is active. This option is enabled by default.

</td></tr><tr><td>

Label

</td><td>

Symbol or label of the KPI unit.

</td></tr><tr><td>

Unit family

</td><td>

Category under which the unit is listed. For example, the unit **US Dollars** is listed under the **Currency** Unit family.**Note:** You can see the list of existing Unit families by selecting the look-up \(\[Omitted image "look-up-icon.png"\] Alt text: Look-up icon\) icon. If none is listed, you can create one by selecting **New**.

</td></tr><tr><td>

Description

</td><td>

Brief description of the KPI unit.

</td></tr><tr><td>

Name

</td><td>

Name of the KPI unit.

</td></tr><tr><td>

Format

</td><td>

Format in which the value is displayed.For example:

-   If Format is $\{0\}, $&lt;value&gt; is displayed.
-   If Format is \{0\}%, &lt;value&gt;% is displayed.


</td></tr><tr><td>

Domain

</td><td>

Domain category under which the unit is listed. By default, the Domain is set as **Global**.**Note:** You can see the list of existing domains by selecting the look-up \(\[Omitted image "look-up-icon.png"\] Alt text: Look-up icon\) icon. If none is listed, you can create one by selecting **New**.

</td></tr></tbody>
</table>5.  Select **Submit**.\[Omitted image "create-kpi-units.png"\] Alt text: Selected button for saving the new KPI unit.

    A record is created for the new KPI unit.


**Parent Topic:**[Configure Supplier Relationship and Performance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/configuring-supplier-performance-mgmt.md)

**Related topics**  


[Create KPI performance domains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-kpi-domain.md)

[Create manual KPI templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-kpi-template-slo.md)

[Create KPIs by adding suppliers to a KPI template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-supplier-kpi-template.md)

