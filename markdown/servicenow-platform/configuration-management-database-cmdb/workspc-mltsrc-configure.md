---
title: Configure the CMDB 360 dashboard in CMDB Workspace or in Service Graph Workspace
description: Configure CMDB 360 settings to determine how your CMDB 360 data is analyzed and aggregated. These settings affect the data that appears on the cards and the records shown when you drill down on those cards in the CMDB 360 dashboard in CMDB Workspace or in Service Graph Workspace.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CMDB 360 experience in a workspace, CMDB 360, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the CMDB 360 dashboard in CMDB Workspaceor in Service Graph Workspace

Configure CMDB 360 settings to determine how your CMDB 360 data is analyzed and aggregated. These settings affect the data that appears on the cards and the records shown when you drill down on those cards in the CMDB 360 dashboard in CMDB Workspaceor in Service Graph Workspace.

## About this task

For detailed information about CMDB 360-related components, such as system properties, scheduled jobs, and tables, see [Components installed with CMDB Workspace](../reference/installed-with-cmdb-workspace.md) or [Components installed with Service Graph Workspace](../reference/installed-with-sg-workspace.md).

## Before you begin

To access the CMDB 360 dashboard in Service Graph Workspace, you must first switch from CMDB Workspace to Service Graph Workspace. For more information, see [Service Graph Workspace store app](../concept/sg-workspace.md).

Role required: cmdb\_ms\_admin

## Procedure

1.  Open either workspace:

2.  -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Insights icon and in the Insights page navigation panel, select **CMDB 360**.
-   Navigate to **Workspaces** &gt; **CMDB Workspace**, and then in the CMDB Workspace menu bar, select **CMDB 360**.
3.  Select **Settings**.

4.  Configure Global settings.

    The **Maximum number of records in a list view** setting determines the maximum number of records that can show when you drill down on the cards in the CMDB 360 dashboard \(drill-down set\). If the total number of returned records is greater than the specified setting value, the dashboard trims the list view output according to this setting and the settings of individual cards.

    You can use this setting to limit the number of records that CMDB 360 must process. The setting applies to these cards:

    -   CIs not reported by discovery sources
    -   Data mismatch
    -   Coverage: CIs with a single discovery source
    -   Coverage: CIs by number of discovery sources
    The CMDB 360 dashboard defaults this value to 100,000.

5.  Configure Potential issues settings.

    These settings affect the calculations for cards on the CMDB 360 view/Potential Issues tile and the list of CIs that appear when you drill down on those cards.

    1.  Configure CIs not reported by discovery sources.

        The **Number of days since CIs were last discovered by a discovery source** setting determines the number of days used in the calculation of the CIs not reported by discovery sources card. The card shows CIs that are discoverable by multiple sources, but at least one discovery source hasn't reported on that CI in the specified number of days.

    2.  Configure Data mismatch.

        These settings determine the classes of CIs included in the calculation and in the drill-down list views of the Data mismatch card. These settings determine which classes to use for the card and the relative weight \(%\) of each of those classes in the card calculations.

        Using these settings, add the classes for which you are interested in seeing CMDB 360 mismatch data. Regardless of the classes that you add in the Data mismatch settings, the ‘Maximum number of records in a list view’ setting, is always in effect when you drill down the card \(100,000 by default\).

<table id="table_a2k_xmz_dvb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automatic data weights

</td><td>

Evenly distributes weights among any added classes. The global setting of ‘Maximum number of records in a list view’ is evenly divided between all added classes so that each class can contribute an equal number of records to the drill-down set.

 For example, if you added four classes, the weight of each class = 25. Therefore, the system adds to the set of drill-down records, up to 25,000 CMDB 360 records \(25% of 100,000\) of each added class.

</td></tr><tr><td>

Manual data weights

</td><td>

Custom weight \(%\) for each added class. The global setting of ‘Maximum number of records in a list view’ is divided between the added classes, according to the specified class weights.

 For example, if you added two classes, class A weight = 25 and class B weight = 75. The system adds to the set of drill-down records, up to 25,000 CMDB 360 records \(25% of 100,000\) of class A, and up to 75,000 CMDB 360 records \(75% of 100,000\) of class B.

</td></tr><tr><td>

Select CI classes you want to include in the calculation

</td><td>

Specify the CI classes that you want to check for attribute mismatches. CI classes you specify also include any child classes. Attributes are considered mismatched when different discovery sources report different values for the attribute.

</td></tr><tr><td>

Show CIs where EVERY attribute doesn't match

</td><td>

Select to include only CIs with a mismatch between discovery sources for every attribute that you specify.

</td></tr><tr><td>

Show CIs where ANY attribute doesn't match

</td><td>

Select to only include CIs with a mismatch between discovery sources for any attribute you specify.

</td></tr><tr><td>

Select an attribute

</td><td>

Specify the attributes that you want to check for mismatches.

</td></tr></tbody>
</table>6.  Configure Coverage settings.

    These settings affect the calculations related to the coverage cards \(‘Coverage: CIs with a single discovery source’ and ‘Coverage: CIs by number of discovery sources’\) in the Discovery Sources tile on the CMDB 360 view. These settings determine the mixture of classes in the drill-down set of records.

    Using these settings, you can give priority to classes for which you are most interested in seeing CMDB 360 data in the Coverage charts. The number of records that you can drill down to in the Coverage charts, is limited by the global setting ‘Maximum number of records in a list view’ \(100,000 by default\). Regardless of your settings and class priorities, the ‘Maximum number of records in a list view’ setting, is always in effect.

    By default, the classes of the records in the drill-down set are random. You can add classes in this Coverage settings to ensure that your preferred classes have priority in being included in the drill-down set of records. You can prioritize any number of classes and assign a weight \(%\) for each of those classes within the total number of drill-down records.

<table id="table_ldr_cnz_dvb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automatic data weights

</td><td>

Evenly distributes weights among any added classes. The global setting of ‘Maximum number of records in a list view’ is evenly divided between all added classes so that each class can contribute an equal number of records to the drill-down set.

 For example, if you added four classes, the weight of each class = 25. Therefore, the system adds to the set of drill-down records, up to 25,000 CMDB 360 records \(25% of 100,000\) of each added class.

</td></tr><tr><td>

Manual data weights

</td><td>

Custom weight \(%\) for each added class. The global setting of ‘Maximum number of records in a list view’ is divided between the added classes, according to the specified class weights.

 For example, if you added two classes, class A weight = 25 and class B weight = 75. The system adds to the set of drill-down records, up to 25,000 CMDB 360 records \(25% of 100,000\) of class A, and up to 75,000 CMDB 360 records \(75% of 100,000\) of class B.

</td></tr><tr><td>

Select CI classes you want to include in the calculation

</td><td>

Prioritized classes for which you are most interested in seeing CMDB 360 data in the Coverage charts \(‘CIs with a single discovery source’ and ‘CIs by number of discovery sources’\).CI classes that you specify also include any child classes.

</td></tr></tbody>
</table>    Using the Coverage settings, the system calculates an allowance of records per class, in the drill-down set of records. If the number of actual records per added class, is less than the computed allowance for that class, then the system adds records of random classes, up to the computed allowance for the class.

7.  Select **Save**.


