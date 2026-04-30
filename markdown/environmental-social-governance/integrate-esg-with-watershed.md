---
title: Integrating ESG Management \(formerly ESG\) with Watershed
description: Watershed is a tool that enables organizations to measure their carbon emissions and renewable energy and its impact. It also enables organizations to act to reduce emissions, and to report on the progress to reduce their carbon footprint.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Integrating ESG Management \(formerly ESG\) with Watershed

Watershed is a tool that enables organizations to measure their carbon emissions and renewable energy and its impact. It also enables organizations to act to reduce emissions, and to report on the progress to reduce their carbon footprint.

ESG Management users can use Watershed to calculate their Scope 1, 2, and 3 emissions for their business. A company’s greenhouse gas \(GHG\) emissions are classified into three Scopes. The following table explains the difference between each Scope.

<table id="table_cn1_xvk_jtb"><thead><tr><th>

Scope 1

</th><th>

Scope 2

</th><th>

Scope 3

</th></tr></thead><tbody><tr><td>

Direct GHG emissions from the following sources:-   Fuel combustion
-   Emissions from company vehicles
-   Emissions from chemical production in owned or controlled process equipment
-   Fugitive emissions

</td><td>

Indirect emissions from the following sources:-   Purchased electricity
-   Heat and steam.

</td><td>

Indirect emissions from the following sources:-   Purchased goods and services
-   Business travel
-   Employee commuting
-   Waste disposal
-   Use of sold products
-   Transportation and distribution \(up- and downstream\)
-   Investments
-   Leased assets and franchises

</td></tr></tbody>
</table>Watershed maintains its data in spreadsheets and provides those spreadsheets to the ESG Management program manager. As an ESG Management program manager, with the role sn\_esg.program\_manager, you must import the data from the spreadsheets into the source tables in the ESG Management application. The source tables are then specified in the metric definitions in a ServiceNow instance.

To use the features of Watershed, you must activate the Operational Sustainability Integration with Watershed plugin and [configure the metric integrations.](../../metrics/task/configure-metric-integrations.md)

**Note:**

-   To successfully import data, you must add the import\_admin role to the sn\_grc\_metric.admin role.
-   Only automated metric definitions with **External source** as the Method type support data import. If you already have a manual metric definition in your system, you must change its Type to **Automated** and the Method type to **External source** before you can import data. For more information, refer to [Create an automated metric definition](../../metrics/task/create-metric-definition.md).

Before you import data from the spreadsheets, you can either create the metric definitions or you can rely on the system to create placeholders and add the details later.

The metrics are generated based on the frequency that you have defined in the metric definition. The metric values, along with their units, are displayed on the metrics related list in the metric definition. The values are then rolled up based on the formula specified in the metric definition.

**Note:** You can convert any metric data into a preferred reporting unit.

By default, the ServiceNow AI Platform provides the following data that you can import from Watershed.

-   Carbon emissions
-   Renewable energy
-   Non-renewable energy

You may also want to import other data such as water usage or waste disposal. To import other types of data, you can use the [Metric integrations](../../metrics/concept/metric-integration.md) to import your data.

-   **[Modify the Operational Sustainability Integration with Watershed](../../metrics/task/configure-metric-integrations.md)**  
Modify the Operational Sustainability Integration with Watershed configurations to specify how you want to import data from Watershed to generate metrics.
-   **[Create data mapping](../../metrics/task/create-data-mapping.md)**  
Create data mappings to import Watershed data from columns other than the pre-configured columns of the Watershed spreadsheet. By default, data import from three columns is supported.
-   **[Create a record identifier in an entity](../task/create-an-entity-mapping.md)**  
Create record identifiers with text for correctly mapping the entities. This activity saves time for the ESG program managers by not having to create new entities.
-   **[Load data from Watershed into ESG Management](../task/load-data-from-watershed.md)**  
Load data from the Watershed spreadsheets into the staging table. After you load the data and complete the setup, you can start using the Operational Sustainability Integration with Watershed.
-   **[View and verify the import sets](../task/view-and-verify-the-import-sets.md)**  
Verify if your data is imported correctly from an external source. This verification enables you to identify if there were any errors during the data import.
-   **[Create a transform map](../task/create-a-transform-map.md)**  
Create a transform map to match the columns from the staging table to the columns in the target table. The transformation helps to convert the data from the source table into metric data.

**Parent Topic:**[Integrating ESG Management \(formerly ESG\) with other applications](integrate-esg.md)

