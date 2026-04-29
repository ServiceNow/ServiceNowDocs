---
title: Create an ETL transform map
description: IntegrationHub ETL provides a guided setup which walks you through the completion of all necessary tasks for creating an ETL transform map for a specific integration.Provide basic details for the integration, such as the source of the data that you want to integrate into CMDB, and import the source data.Review sample records of raw source data, which will be integrated into the CMDB. Transform and prepare data to align with the target classes and attributes, if needed.There are several requirements and guidelines for mapping source data to target CMDB classes and attributes. Also, there is an option of deactivating class mappings while preserving the settings for an easy reactivation. Review these concepts to ensure proper processing by the Identification and Reconciliation Engine \(IRE\).Choose target classes and attributes in the CMDB to map source data columns to. You can map a data column to a specific target class, or add conditions so that the choice of target class depends on specific data values.Add relationships that exist among the target CMDB classes, for an integration.Preview the results of the sample data integration.Configure a schedule for importing data to CMDB using this ETL Transform Map.Use various transforms in IntegrationHub ETL to convert and prepare source data for mapping to the CMDB.
locale: en-US
release: australia
product: Integration Hub ETL
classification: integration-hub-etl
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 40
breadcrumb: [IntegrationHub ETL, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create an ETL transform map

IntegrationHub ETL provides a guided setup which walks you through the completion of all necessary tasks for creating an ETL transform map for a specific integration.

## Guided setup

Guided setup organizes all the tasks in the correct order, tracks the completion of tasks, and enforces any task dependencies. Tasks that depend on the completion of other tasks, are enabled or disabled as you step through the tool and complete tasks.

Use guided setup on the ETL Transform Map Assistant page to complete the following tasks.

## Import source data and specify basic details

Provide basic details for the integration, such as the source of the data that you want to integrate into CMDB, and import the source data.

### Before you begin

The data source that you plan to select for the ETL Transform Map must exist in the same application scope as the one being used in the current session.

When you open an ETL transform map, by default the map is not validated. You can enable this validation step by [adding the system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) **sn\_int\_studio.validation.enabled** to the System Properties \[sys\_properties\] table and then setting it to **true**. After validation is complete, you choose how to handle validation errors.

Role required: cmdb\_inst\_admin

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**.

    The landing page of the IntegrationHub ETL lists all integrations that exist in the system, including integrations that were downloaded from the ServiceNow Store. Starting with IntegrationHub ETL v3.2, integrations are grouped by the **CMDB Application** value, in which case expand the respective group to locate an integration.

2.  Click the **Name** of an integration to view or modify, or click **Create new**.

    If the system property **sn\_int\_studio.validation.enabled** is set to **true**, then IntegrationHub ETL validates the ETL transform map that you are loading. If there are any validation errors, the Invalid Mapping Data Detected dialog box appears, listing all the specific errors that were detected. You can choose to delete the invalid mappings and continue with only the valid mappings, or you can choose to keep the invalid mappings. However, notifications about invalid mappings will continue to appear as you continue to work with the integration.

    The system detects errors such as:

    -   Missing source or target fields in corresponding Robust Transform Engine \(RTE\) field mappings records
    -   Missing table columns in an import set

        **Note:** In this situation, any corresponding metadata records in RTE are no longer valid and are automatically deleted. Records such as field mappings and transform operations that are associated with the missing table columns in the import set, are deleted.

    -   Missing an Identification and Reconciliation Engine \(IRE\) lookup rule for a lookup class
3.  On the ETL Transform Map Assistant page, in the Specify Basic Details section of the guided setup, select the **Import Source Data and Provide Basic Details** task.

4.  Fill out the form.

<table id="table_u5c_mqc_ckb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CMDB Application

</td><td>

The CMDB application associated with the ETL transform map.

 You can select **Add new**, which adds the **CMDB Application** and the **Discovery Source** fields for the new CMDB application.

</td></tr><tr><td>

Name

</td><td>

Name of the ETL transform map.

</td></tr><tr><td>

Description

</td><td>

Description of the integration.

</td></tr><tr><td>

Data Source

</td><td>

List of all data sources in the system.**Note:** Be cautious in subsequently modifying the data source as it can result in substantial changes to the data integration. Aligning to the import set table of the new data source might require the removal of columns and associated transforms, or the addition of new columns. IntegrationHub ETL validation processes will detect any required updates and let you agree or reject these updates.

</td></tr><tr><td>

Sample Import Set

</td><td>

An Import Set that is associated with the specified **Data Source**.

 A subset of that Import Set data is used to preview source data.

 Select the **Auto-pull a new import set** option to pull a new Import Set of the associated data source.

 Starting with IntegrationHub ETL v3.2, if no Import Set is specified, then the map is loaded and is automatically set to be in read-only mode. You can review configurations in the map but can’t edit mappings or transforms.

</td></tr><tr><td>

Preview Size Override

</td><td>

Number of data records that are loaded and used as sample for the preview for this transform map. If set, this custom setting overrides the value of the **sn\_int\_studio.preview.size** system property, and applies only to the current transform map.

 If **Load Complete Schema** is disabled, then the nested data structure for the map is generated based only on the specified number of records that are loaded.

 Field available starting with IntegrationHub ETL v3.2.

</td></tr><tr><td>

Load Complete Schema

</td><td>

Enable or disable loading the entire data schema for generating the data structure for the map.

 When disabled, the nested data structure for the map is generated based only on the number or records loaded as sample records for preview. The number of records loaded is determined by either the **Preview Size Override** setting, or by the global system property **sn\_int\_studio.preview.size**.

 Field available starting with IntegrationHub ETL v3.2.

</td></tr><tr><td>

CMDB Application

</td><td>

Name of a new **CMDB Application**. Appears if you set **CMDB Application** to **Add new**.

</td></tr><tr><td>

Discovery Source

</td><td>

Discovery source associated with a new **CMDB Application**. Appears if you set **CMDB Application** to **Add new**.

</td></tr></tbody>
</table>5.  Click **Save** to save the current changes or **Mark as Complete**.

    A time stamp appears in the header when you click **Save**, which remains for the duration of the IntegrationHub ETL session for the ETL transform map. When you re-enter the session or switch between ETL maps, the time stamp disappears.


**Related topics**  


[Create an Import Set data source](https://www.servicenow.com/docs/access?context=c_CreateNewDataSource&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

## Preview and prepare data

Review sample records of raw source data, which will be integrated into the CMDB. Transform and prepare data to align with the target classes and attributes, if needed.

### Before you begin

The number of records in the sample data is globally determined by the system property **sn\_int\_studio.preview.size**, which is set to 100 by default. The maximum number of records in the sample data that IntegrationHub ETL can process is 10,000. If you set that property above the 10,000 limit, then IntegrationHub ETL will only process up to 10,000 records and a message will appear to that effect.

Starting with IntegrationHub ETL v3.2, you can override the value of the **sn\_int\_studio.preview.size** property by setting the **Preview Size Override** field on the Import Source Data and Provide Basic Details form, per map.

To process nested data from a nested payload, the respective data source must be set with the **Data in single column** option.

Role required: cmdb\_inst\_admin

### About this task

Review the values in the data columns of the sample data and identify columns that do not align with the requirements of the intended target classes and attributes. You can transform data, for example, by converting the data format, replacing values, and concatenating data columns. You can apply transformations one on top of another, creating a chain of data transformations. You can also set a data column to be ignored in the mapping and integration process.

**Note:** To set a CMDB attribute to be empty, use the string '&lt;EMPTYֹ\_STRING&gt;'.

Columns for nested data appear alongside the rest of the data, with a **Nested Objects** notation in the data column header. The count of nested data items per object appear with a link which lets you drill to deeper levels of the nested data. To show the data structure of nested data in a separate panel, enable the **Show data structure** option.

The Data Structure panel has two options for displaying nested data:

-   **Tree**: Nested data grouped by objects, where each object node corresponds to a record entry in the source data. Expand object nodes to show all nested data for the record.
-   **Collection**: Nested data grouped by the top-level object \(by default\) and then by nested data items such as software. Expand a node such as software, to show which software is installed on each computer.

You can navigate through the levels of nested data in the Data Structure panel, the breadcrumbs path, or through number links that appear in the source data itself. Your selections and the data that appears are kept synchronized between all views of the nested data, regardless of navigation.

For a demo about working with nested payload data, watch the [Integration Hub - ETL nested payload feature demo](https://youtu.be/jonkMkFiNaQ) video on the ServiceNow YouTube channel.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**, and click the **Name** of an integration.

    The landing page of the IntegrationHub ETL lists all integrations that exist in the system, including integrations that were downloaded from the ServiceNow Store.

2.  In the ETL Transform Map Assistant page, in the Prepare Source Data for Mapping section of the guided setup, select **Preview and Prepare Data**.

3.  Select **Show data structure** to open the Data Structure panel which shows the structure of nested data. In the Data Structure panel, you can drill down through the levels of nested data.

4.  Select the action menu for a column and then select a Sort operation.

5.  Select the action menu for a column and then select **Group by** to group the data by the respective column. Select **Ungroup** to undo the grouping operation.

6.  Click **New Transform** and then select **Use Source Column** . Or, select the action menu for a column, and then select **New Transform** to transform the selected column.

    You can't create new transforms for nested objects at this top-level view of the data. A nested object column contains number links which indicate the number of nested items for the record. To create a new transform for nested objects, click that number link to drill down to the actual nested data. Alternatively, navigate in the Data Structure panel to the nested object for which you want to create a transform.

    A transform of nested data can reference parent objects of the nested data being transformed. Using the [sample payload for nested data](integrationhub-etl.md) as an example, a transform for an interface object can reference the parent computer object but can't reference a software object.

    1.  In the New Transform sidebar on the right, select a **Transform Type** and modify the **Transform Description** if appropriate.

        For more details about transform types, see [Transform types in IntegrationHub ETL](create-etl-transform-map.md#).

    2.  Select **Hide initial column used for this transform** to hide from the current view all the columns that were used for this transform.

        This setting is temporary for the current session, and if you refresh the page, the hidden column reappears. To show a hidden column, you can also click the gear icon on the banner frame. Then, move the hidden column from the Available to the Selected list and click **OK**.

    3.  Select or verify the **Input Column** whose values are being transformed.

    4.  Modify the **Output Column Name** for any of the columns that will be added with the transformed values.

    5.  Click **Apply**.

        A new column with the transformed values appears, placed in alphabetical order based on the output column name. If you used the suggested output column name, then the new column appears to the right of the input column.

    6.  Review the transformed data and adjust any transforms, if needed.

7.  To apply the 'Set Fixed Value Column' transform:

    1.  Click **New Transform** and then select **Set Fixed Value Column**.

    2.  In the Set Fixed Value Column sidebar, enter a **Column Name** and a **Column Description** for the new column. Then, set **Assign Column Value** to the value that is fixed for the new column.

    3.  Click **Apply**.

8.  Select the action menu for a column, and then select **Ignore in Mapping** to exclude the column from mapping and integration in the current session.

    In a subsequent session, the **Ignore in Mapping** setting does not apply, and the column will be included in mapping.

    You can click **Include in Mapping** to undo the **Ignore in Mapping** setting for the column.

9.  Select the action menu for a column, and then select **Delete This and Downstream Columns**. This delete action deletes the column along with any columns that were added using this column as an input column.

10. Click **New Transform** and then select **Table Lookup** which lets you specify a table to look up and extract additional values from. Fill out the fields in the Table Lookup sidebar on the right.

    Values from the specified lookup table are matched with the mapped data. For the records that match, the specified values from the lookup table, are added as a column, to the data that is being prepared for mapping.

<table id="table_xmg_xt4_rkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lookup Table

</td><td>

Table to use for matching with the data that is being mapped. When records from the lookup table and the mapped data satisfy the **Look Up Condition**, then specified values from the **Lookup Table** are extracted from the respective record and added to the mapped data.

</td></tr><tr><td>

Lookup Condition

</td><td>

A set of pairs of column conditions. Each pair specifies a column in the lookup table and a column in the mapped data, which are attempted to be matched.

 -   **If values of target table column**: The column in the target table to match to a column in the mapped data.
-   **Match values of source data table**: The column in the mapped data to match to a column in the lookup table.
 You can add multiple pairs of columns to match on.

</td></tr><tr><td>

Lookup Condition

</td><td>

Values to extract from the **Lookup Table** when there is a match with the mapped data.

 **Then output values from the following columns**: The lookup table columns to extract values from, when values from the lookup table and the mapped data, satisfy the **Lookup Condition**.

 You can specify multiple lookup table columns to extract values from. For every column that you specify, a corresponding **Output Column Name** field automatically appears. Specify a label for the column that will be added with the extracted values.

</td></tr><tr><td>

Output Column Name

</td><td>

A label for the column that will be added to the mapped data, with the values extracted from the lookup table.

 An **Output Column Name** field is automatically added for every column that you specify in **Then output values from the following columns**.

</td></tr></tbody>
</table>11. Review the data and ensure that the intended set of data to be integrated is transformed, correctly formatted and prepared for import.

12. Click **Mark as Complete**.


### Result

Data is prepared when the set of source data columns and transformed columns that you want to integrate, meet any formatting and other value requirements of the target CMDB classes and attributes. These columns are then ready to be mapped and integrated to CMDB classes and attributes.

## About mapping data columns to CMDB classes and attributes

There are several requirements and guidelines for mapping source data to target CMDB classes and attributes. Also, there is an option of deactivating class mappings while preserving the settings for an easy reactivation. Review these concepts to ensure proper processing by the Identification and Reconciliation Engine \(IRE\).

### Required mappings

You must map data to all required attributes of the target class in addition to mapping to attributes that are not configured as required. Also, the following two fields appear by default and you cannot delete them:

-   **Source Native Key**

    IRE uses to uniquely identify a record and for building relationships and references. Also, improves performance of insert and update operations. When processing a payload, IRE generates an error if this field is empty.

-   **Source Recency Timestamp**

    IRE uses to identify records that are older than the current record and therefore can be ignored, to help resolve conflicting attribute values. If a value is provided, it is used only if it is later than the value that is currently stored in the CMDB. If a value is not provided, IRE updates the attribute with the current timestamp.

    The following system properties let you modify how IRE uses the **source\_recency\_timestamp** value in a payload to update the **last\_scan** attribute in the Source \[sys\_object\_source\] table:

    -   [glide.identification\_engine.skip\_updating\_last\_scan\_if\_older](../reference/properties-id-reconciliation.md)
    -   [glide.identification\_engine.ire\_message\_listener\_skip\_updating\_last\_scan\_to\_now](../reference/properties-id-reconciliation.md)

For more information about how IRE uses **source\_native\_key** and **source\_recency\_timestamp** for CI identification, see [Identification and Reconciliation engine \(IRE\)](ire.md).

### Conditional class

A conditional class lets you map different sets of data records to different target classes according to specific column values, or the status of a specific plugin.

For example, if a display name contains 'Windows', then 'Windows Server' is selected as the target class. But if the display name contains 'Linux', then 'Linux Server' is selected as the target class. For records that do not meet any of these conditions \(display name does not contain 'Windows' nor 'Linux'\), 'Server' is selected as the target class.

### Associated class

An associated class lets you select the CMDB class to be associated with a target non-CMDB table. Setting an associated class is required for IRE processing if the non-CMDB table is not configured for IRE processing. For a non-CMDB table that is supported and configured for IRE processing, setting an associated class is optional. See [IRE support for non-CMDB tables](ire-support-non-cmdb-tables.md) for more information.

The software Instance is a non-CMDB class but it does not have IRE rules associated with it. So, things we said about it here pre-Utah are still valid. But for non-CMDB classes with IRE rules it's not mandatory to have an association. For example “If the target class for mapping is a non-CMDB class with a reference to a CMDB class, you must select the CMDB class to associate the non-CMDB target class with” non-CMDB class with IRE rules Instead of “you must” it should be. “You can”. Same with the Example it's not valid for non-CMDB with IRE rules.

If the target class for mapping is a non-CMDB class with a reference to a CMDB class, you must select the CMDB class to associate the non-CMDB target class with. A non-CMDB class refers to a class, such Serial Number \[cmdb\_serial\_number\], that does not extend the Configuration Item \[cmdb\_ci\] class. The Related Entry \[cmdb\_related\_entry\] class might contain multiple CMDB class associations for the same non-CMDB class. Therefore, select the appropriate association to allow IRE processes to update the target non-CMDB class.

For example, the Related Entry \[cmdb\_related\_entry\] class has a record which associates the non-CMDB Software Instance \[cmdb\_software\_instance\] class with the CMDB Software Package \[cmdb\_ci\_spkg\] class. If you select Software Instance as a target class, you must associate the Software Instance class with the Software Package \[cmdb\_ci\_spkg\] class.

### Deactivating class mappings

When you edit an ETL transform map, provided by a Service Graph Connector for example, you can delete a class mapping to prevent the class from being populated when the integration runs. However, if you later decide to populate that class, you must readd that class and reconfigure all the class mappings. Instead, you can deactivate a class mapping to temporarily ignore the class during the integration run, while preserving all of its mapping configuration. A class that you choose to deactivate is grayed out in the user interface but you can continue and edit the class mappings. Later, you can reactivate a class mapping to enable populating the class, without needing to reconfigure the class mappings.

Some classes that you choose to deactivate, trigger an automatic deactivation of additional classes that you did not directly choose to deactivate. Which classes are automatically deactivated, depends on the class that you chose to deactivate. For example, whether the class has dependent relationships or associated classes. Those automatically deactivated classes:

-   Appear in light gray in the user interface and you can't reactivate them.
-   Are automatically reactivated when you reactivate:
    -   The class that you initially deactivated which triggered the automatic deactivation
    -   Any class that the deactivated class depends on

All classes that you directly deactivate mappings for and the resulting class mappings that are automatically deactivated, are not populated when the integration runs. Also, any relationships and lookup tables associated with those classes, are not populated when the integration runs.

Class mapping and other deactivation scenarios:

-   Deactivate a class which no class depends on and which has no associated classes:

    Triggers an automatic deactivation of any lookup rules and relationships associated with the deactivated class.

-   Deactivate a lookup rule, such as serial number, within a class mapping:

    Does not trigger any automatic deactivations.

-   Deactivate a CMDB class which is associated with a non-CMDB class:
    -   Triggers an automatic deactivation of the associated non-CMDB class.
    -   Deactivating the non-CMDB class, does not impact the associated CMDB class.
-   Deactivate a class with dependent relationships \(Applies only if the dependent relationship exists in IntegrationHub ETL\):

    -   Triggers an automatic deactivation of any class that has a single dependent relationship with the deactivated class.
    -   If a class has multiple dependent relationships, then it is automatically deactivated only when you deactivate all of the dependent on classes.

        For example, a scenario in which the File System class has dependent relationships with both, the Computer and a Server class. If you deactivate the Computer class, the File System class is not automatically deactivated. Only if you also deactivate the Server class, the File System class is automatically deactivated.

-   Deactivate a conditional class or a class mapping within a conditional class:
    -   Deactivating or activating a conditional class, triggers an automatic deactivation or activation of all conditional class mappings within the conditional class.
    -   Deactivating a class mapping within a conditional class: Prevents the deactivated class from getting populated during integration runs. However, the associated 'If', 'Else if', or 'Else' conditions themselves remain in effect within the condition of the conditional class. For example, if you deactivate the following class mapping:

        **\[If\] \[operating\_system\] \[contains\] \[Linux\] Then \[Class\] \[is\] \[Linux Server\].**

        Then, the Linux Server class is not populated, but the **\[If\] \[operating\_system\] \[contains\] \[Linux\]** condition is in effect.


## Map data columns to CMDB classes and attributes

Choose target classes and attributes in the CMDB to map source data columns to. You can map a data column to a specific target class, or add conditions so that the choice of target class depends on specific data values.

### Before you begin

Role required: cmdb\_inst\_admin

### About this task

Data columns that you map can be either source data columns which were not transformed, or transformed data columns. For example, to integrate a data column into the Computer and Software Package classes, select those classes as target classes and then map data columns into specific attributes in those classes.

When you configure mapping for a class, relationship, or a lookup rule, those items are always initially set as activated. For details about the results of deactivating mappings, see [Deactivating class mappings](create-etl-transform-map.md#).

**Note:** Changing a class impacts any mappings that were already configured for the class, sometimes deleting those mappings. Details about the affected mappings and the impact, appear in the Affected mappings dialog box before you proceed with the class change. However, these details appear only when the change is from a CMDB class to another CMDB class or from a non-CMDB class to another non-CMDB class.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**, and click the **Name** of an integration.

    The landing page of the IntegrationHub ETL lists all integrations that exist in the system, including integrations that were downloaded from the ServiceNow Store.

2.  In the ETL Transform Map Assistant page, in the Map Data to CMDB and Add Relationships section of the guided setup, select **Select CMDB Classes to Map Source Data**.

    Attributes that are configured as required in the platform, are noted, and you must map a data column to each of those attributes.

3.  Click **Add Class** to add a target class to map to, or click **Edit Class** to edit a class.

    1.  In the Add Class dialog box, select a CMDB **Class**.

    2.  Click **Save**.

    3.  Set the **Activate/Deactivate Mapping** toggle switch for a class, to on or off. If the Affected class mappings dialog box appears, review the list of affected classes, and then click **Proceed**.

        When you add a non-CMDB class, it is initially deactivated and the **Activate/Deactivate Mapping** toggle switch is disabled, until you add an associated class that is active.

4.  Click **Add Conditional Class** and then in the **Add Conditional Class** dialog box, specify the conditions that must be met for data to be mapped to different target classes.

    1.  **Collection** is automatically set to the data branch in the hierarchy which is associated with the lowest-level attribute. You can modify the value to the data branch from which you want to map data from, which must be at a higher level in the same data branch of the hierarchy.

    2.  In the **If** drop-down list, select attribute conditions that data values must meet, or enter `plugins` in the search box and specify a plugin condition. You can then specify that the rest of the records, which did not match any conditions, are mapped to yet a different target class. Data records will be mapped to different target classes according to the conditions met.

        When processing nested data, a prefix denotes the first level in the nested hierarchy for attribute items.

        **Note:** When you select a non-CMDB class, it is initially deactivated and the **Activate/Deactivate Mapping** toggle switch is disabled, until you add an associated class that is active.

    3.  Click **Save**.

    4.  Set the **Activate/Deactivate Mapping** toggle switch for a conditional class, to on or off. If the Affected class mappings dialog box appears, review the list of affected classes, and then click **Proceed**.

    5.  Click **Edit Class** to edit the settings of a conditional class. In the Edit Conditional Class dialog box, set the **Activate/Deactivate Mapping** toggle switch for a class mapping, to on or off. Click **Save**, and if the Affected class mappings dialog box appears, review the list of affected classes and then click **Proceed**.

        -   A deactivated class is not populated during integration runs, however, this doesn't affect the associated condition. The 'If', 'Else if', and 'Else' conditions themselves remain in effect within the condition of the conditional class and matching CIs are filtered accordingly.
        -   The toggle switch of the conditional class reflects the summary of the states of all the conditional class mappings within the conditional class. If at least one of the conditional class mappings is activated, then the toggle switch of the conditional class appears as activated. Otherwise, the toggle switch of the conditional class appears as deactivated.
5.  For a non-CMDB class, click **Add Associated Class** to associate the non-CMDB class with a CMDB classand to enable the **Activate/Deactivate Mapping** toggle switch.. Or, click **Edit Associated Class** to edit an already associated class.

    1.  In the Add Associated Class dialog box, select a CMDB class. The list includes all entries in the Related Entry \[cmdb\_related\_entry\] class for the specified non-CMDB table\(deactivated classes are not included\).

    2.  Click **Add**.

    3.  Set the **Activate/Deactivate Mapping** toggle switch for an associated class, to on or off.

        **Note:** If an associated class was not added or is deactivated, then the **Activate/Deactivate Mapping** toggle switch is disabled.

6.  Click **Set Up Mapping** to configure mapping for a newly added class, or click **Edit Mapping** to edit a mapping.

    1.  To map, drag data columns from the Data sidebar on the right, to CMDB target attribute on the left side of the mapping page. Or, click the ![Select a column in IntegrationHub ETL.](../image/IntegrationSelectDataColumn.png) icon to search and select data columns for the mapping.

        When mapping nested data:

        -   Data columns in the Data sidebar appear in a tree format that represents the structure of the nested data. Each attribute is associated with sample data for the attribute.
        -   Transformed columns are noted by a cyan-shaded dot.
        -   All mappings to a specific CMDB class must be from the same source branch in the nested data. Only the branch from which you selected the first column to map, is valid for selecting columns in subsequent mappings.

            This restriction applies differently when mapping to attributes in lookup tables. All mappings to attributes in a lookup table also must be from the same source branch. However, that source branch can be different than the source branch you used with non-lookup tables.

            **Note:** You can work around this restriction by using the [Copy](create-etl-transform-map.md#) transform in the data preparation step, to copy attributes from a parent level to a child level. Prepare the data so that all the attributes that you want to map, are at the same level.

        -   When you drag a column to map from the Data sidebar, the fields of CMDB target attributes that are valid for the mapping, are highlighted by a green frame. If you attempt to drop a column in an invalid target attribute, the respective field is highlighted by a red frame and an error appears.
    2.  Click **Add Attribute**. Then, in the Add Attribute dialog box, from the **Attribute** list, select one or more items as target attributes to map data to. You can also scroll down to the **IRE Settings** section of the list and select one of the [robust import set transformer properties](https://www.servicenow.com/docs/access?context=robust-import-set-xform-props&version=australia&pubname=australia-integrate-applications&ft:locale=en-US). Click **Save**.

        For information about precedence order between robust import set transformer properties defined at the individual item level and at the IRE payload level, see [robust import set transformer properties](https://www.servicenow.com/docs/access?context=robust-import-set-xform-props&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) .

    3.  Map any lookup rules such as the 'Serial Number Lookup 1' rule.

        Lookup rules are in a deactivated state until you map them.Click the filter icon for the lookup rule to edit or add any lookup filters. In the lookup filter dialog box, specify attribute or plugin conditions that must be met for data to be mapped to various target classes. Then click **Save**.

        After mapping a field of a lookup rule, you can set the Activate/Deactivate Lookup rule toggle switch for a rule, to on or off.

    4.  Click **View Class Details** to view the current class in [CI Class Manager](../reference/ci-class-manager-landing-page.md).

    5.  Click the **Transform Data** tab to navigate to the data preparation page where you can review and further transform data that you want to map.

    6.  Return to the Select CMDB Classes to Map Source Data page.

7.  Click **Mark as Complete**.


## Add Relationships

Add relationships that exist among the target CMDB classes, for an integration.

### Before you begin

-   A class that you want to add in the relationship, must be in an activated state.
-   A base relationship or a relationship within a conditional relationship, that you want to edit, must be in an activated state.
-   In a conditional relationship that you want to edit, at least one relationship condition must be in an activated state. Otherwise, the **Edit Relationship** button is grayed out.

Role required: cmdb\_inst\_admin

### About this task

When creating relationships with nested data, you can't create a relationship between sibling objects from the nested data. Using the [sample payload for nested data](integrationhub-etl.md) as an example, you can't create a relationship between interfaces and software.

ITOM Visibility, if available, uses enhanced discovery patterns to identify and add CI relationships to the Suggested Relationships table in the base system. When applicable, use the Suggested Relationships table to select relationships that are in compliance with Common Service Data Model \(CSDM\) standards.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**, and click the **Name** of an integration.

    The landing page of the IntegrationHub ETL lists all integrations that exist in the system, including integrations that were downloaded from the ServiceNow Store.

2.  In the ETL Transform Map Assistant page, in the Map Data to CMDB and Add Relationships section of the guided setup, select **Add Relationships**.

3.  To add relationships, select **Add Relationship** or **Add Conditional Relationship** if you want to specify attribute conditions that must be met before adding a relationship. Then, complete the following actions as needed.

<table id="choicetable_rvq_52s_2nb"><thead><tr><th align="left" id="d464469e1742">

Option

</th><th align="left" id="d464469e1745">

Description

</th></tr></thead><tbody><tr><td id="d464469e1751">

**Add Relationship**

</td><td>

1.  Select the **Parent**, **Child**, and **Relationship Type** values.
2.  Click **Add**.


</td></tr><tr><td id="d464469e1781">

**Add Conditional Relationship**

</td><td>

1.  In the **choose field** list, select attribute conditions that the data values must meet.
2.  Select the **Parent**, **Child**, and **Relationship Type** values.
3.  Click **Save**.
 When processing nested data, a prefix denotes the first level in the nested hierarchy for attribute items.

</td></tr></tbody>
</table>    The **Relationship Type** list menu changes based on the selected parent and child class:

    -   If there is a dependent relationship, the list is disabled and the relationship type is automatically populated.
    -   If there is more than one dependent relationship, the list displays both containment and hosting relationship options and the containment relationship type is automatically populated.
    -   If there is no dependent relationship, the list displays **Suggested relationships** with the first suggested relationship automatically selected, followed by the base system relationship types.
    -   If there is no suggested relationship, the list displays **No suggested relationships** followed by the base system relationship types.
4.  Click **Save** to save the current changes or **Mark as Complete**.

    A time stamp appears in the header when you click **Save**, which remains for the duration of the Integration Hub ETL session for the ETL transform map. When you re-enter the session or switch between ETL maps, the time stamp disappears.


## Preview mapping results

Preview the results of the sample data integration.

### Before you begin

Role required: cmdb\_inst\_admin

### About this task

Run an integration test and view a summary of the results, for the sample data \(by default,up to 100 records\). The summary includes total numbers for relationships that were created, mapped classes, partial and incomplete payloads that IRE couldn’t process. You can also view detailed messages from Robust Transform Engine \(RTE\) and from Identification Reconciliation Engine \(IRE\).

**Note:** Most IntegrationHub ETL log messages \(from RTE and IRE\) are informational. However, even if the **com.glide.import\_set.importlog\_level** and the **glide.importlog.log\_to\_table** system properties are set to not add INFO log messages, IntegrationHub ETL does render INFO log messages. For more details about these properties, see [Import sets properties](https://www.servicenow.com/docs/access?context=r_ImportSetsProperties&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

After you view the details in the summary page, you can return to any step to make adjustments and then rerun the integration.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**, and click the **Name** of an integration.

    The landing page of the IntegrationHub ETL lists all integrations that exist in the system, including integrations that were downloaded from the ServiceNow Store.

2.  In the ETL Transform Map Assistant page, in the Preview Sample Integration Results and Schedule Import section of the guided setup, select **Test and Rollback Integration Results**.

3.  On the Test and Rollback Integration Results page, click **Run Integration**.

4.  View the summary page and click the various tabs to see the integration run results for the affected CMDB classes. You can select the preview icon to open CI forms and view information.

    **Note:** The order of the attribute columns follows the default columns list for the class in the platform. First, the default columns for the class appear from left to right, followed by the rest of the attribute columns organized in alphabetical order. For example, to see the default columns list for the Computers class, navigate to **All** &gt; **Configuration** &gt; **Computers**.

5.  Select any class tab and click **Edit Mapping** to return to the Select CMDB Classes to Map Source Data page where you can review and change mapping settings.

    **Note:** Clicking **Edit Mapping** rolls back all the changes that were made to the CMDB as a result of this integration run.

6.  Click the **Relationships** tab and review any relationships that were created.

7.  Click **Edit Relationships** to return to the Add Relationships page where you can review and change any relationship configurations.

    **Note:** Clicking **Edit Relationships** rolls back all the changes that were made to the CMDB as a result of this integration run.

8.  Click the **Error Log**, **Activity Log**, or the **Warning Log** tabs to see the respective details logged by IRE and RTE during the integration.

    IRE log records are grouped by categories and further organized by the respective class. For IRE log messages, the Message column contains only the messages themselves which were extracted from the raw log message. The Log Message column contains the complete log message, which includes class and category in addition to the message itself. RTE logs appear under the Other category.

    Use the **Verbose** toggle switch to change the viewing mode for the Message and the Log Message columns:

    -   Verbose on: Shows fully expanded text of log messages.
    -   Verbose off: Shows a condensed version of the log messages. The fully expanded text of the log messages appears when you point to a message.
9.  Click the **Incomplete Payloads** and **Partial Payloads** tabs for details about IRE payloads for the integration run.

10. Select **Mark as Complete**.

    The Rollback options dialog box appears and you can choose either of the following options.

    -   **Retain Data**: All the changes to the CMDB resulting from this integration, are retained.
    -   **Perform Rollback**: All the changes to the CMDB resulting from this integration, are rolled back and the CMDB is restored to its state before running the integration.

## Provide integration schedule

Configure a schedule for importing data to CMDB using this ETL Transform Map.

### Before you begin

Role required: cmdb\_inst\_admin

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**, and click the **Name** of an integration.

    The landing page of the IntegrationHub ETL lists all integrations that exist in the system, including integrations that were downloaded from the ServiceNow Store.

2.  In the ETL Transform Map Assistant page, in the Preview Sample Integration Results and Schedule Import section of the guided setup, select **Set Import Schedule**.

3.  On the Provide Schedule page, click **Set Schedules**.

4.  In the Scheduled Data Imports list view \(which opens in a new tab\), click **New**.

5.  Fill out the Scheduled Data Import form and then click **Submit**.

    See [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) for details about the form fields.

6.  Click **Mark as Complete**.


## Transform types in IntegrationHub ETL

Use various transforms in IntegrationHub ETL to convert and prepare source data for mapping to the CMDB.

Transforms from the [Integration Commons for CMDB](integration-commons-for-cmdb.md) store app, are also available in IntegrationHub ETL.

### Concatenation

Combines the values from input fields into a single string, joining them on the optional **joining\_string** field.

|Details| |
|-------|---|
|Table|sys\_rte\_eb\_concat\_operation|
|Input fields|**source\_sys\_rte\_eb\_fields**|
|Output field|**target\_sys\_rte\_eb\_field**|
|Additional Fields|**joining\_string** \(optional\)|

|Example| |
|-------|---|
|Input|“input\_1”, “input\_2”, “input\_3”|
|Additional Fields|**joining\_string** = ”, ”|
|Result|“input\_1, input\_2, input\_3”|

### Convert to Boolean

Converts the incoming value to a boolean. ‘`true`’ and ‘`1`’ values convert to 'true' \(case insensitive\), and any other values convert to 'false'.

|Details| |
|-------|---|
|Table|sys\_rte\_eb\_to\_boolean\_operation|
|Input fields|**source\_sys\_rte\_eb\_field**|
|Output field|**target\_sys\_rte\_eb\_field**|

Examples:

-   All of the following inputs return 'true':
    -   true
    -   1
-   All of the following inputs return 'false':
    -   “input\_1”
    -   “”
    -   0
    -   11

### Convert to Date

Attempts to convert the incoming value to a **GlideDateTime** value by applying the **date\_format** to the incoming value. Attempts to directly convert using **GlideDateTime** if the **date\_format** is incorrect.

<table id="table_dfx_2rx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_to\_date\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Returns an empty value if unable to parse at all.

</td></tr><tr><td>

Additional Fields

</td><td>

**date\_format** \(Java simple date format\)

</td></tr></tbody>
</table>|Example| |
|-------|---|
|Input|"2018/09/20 11:21:00 a.m. EST”|
|Additional Fields|**date\_format** = “yyyy/MM/dd hh:mm:ss a z”|
|Result|“2018-09-20 16:21:00”|

|Example| |
|-------|---|
|Input|"2018/09/20 01:21:00 PM EST”|
|Additional Fields|**date\_format** = “yyyy/MM/dd hh:mm:ss a z”|
|Result|“2018-09-20 18:21:00”|

|Example| |
|-------|---|
|Input|"09/20/18”|
|Additional Fields|**date\_format** = “yyyy/MM/dd hh:mm:ss a z”|
|Result|“0018-09-20 00:00:00”|

### Convert to Numeric

Converts the incoming value to a number.

<table id="table_hhy_2rx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_to\_numeric\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** If the incoming value is non-numeric, then the output is empty.

</td></tr></tbody>
</table>|Example| |
|-------|---|
|Input|1.23|
|Result|1.23|

|Example| |
|-------|---|
|Input|1.00|
|Result|1|

|Example| |
|-------|---|
|Input|input\_1|
|Result|null|

|Example| |
|-------|---|
|Input|two|
|Result|null|

### Copy

Copies the source field’s value to all of the target fields.

|Details| |
|-------|---|
|Table|sys\_rte\_eb\_copy\_operation|
|Input fields|**source\_sys\_rte\_eb\_field**|
|Output field|**target\_sys\_rte\_eb\_fields**|
|Additional Fields|**overwrite\_existing\_value** \(optional, boolean\): If **true**, then the values of target fields are replaced. Otherwise, any non-empty value is not overwritten.|

### Extract Leading Numeric

Sets the target field to be the first numeric value found in the source field.

<table id="table_i11_frx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_extract\_numeric\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Additional Fields

</td><td>

-   **decimal\_places** \(optional, number\): Forces the output to have a specified number of decimal places.
-   **remainder\_target\_field** \(optional, reference to a field\): Set to the trimmed remainder of the source field, after removing the first numeric value.

</td></tr></tbody>
</table>|Example| |
|-------|---|
|Input|“100 mb”|
|Result|"100”|

|Example| |
|-------|---|
|Input|“100.123 mb”|
|Result|“100.123"|

|Example| |
|-------|---|
|Input|“100.123 mb”|
|Additional Fields|**decimal\_places** = 2|
|Result|“100.12”|

|Example| |
|-------|---|
|Input|“100 mb”|
|Additional Fields|**decimal\_places** = 2|
|Result|“100.00”|

|Example| |
|-------|---|
|Input|“100 mb”|
|Additional Fields|**remainder\_target\_field** = &lt;field&gt;|
|Result|“100” and &lt;field&gt; = “mb”|

### Glide Lookup

Performs a lookup in the database on the **target\_table**.

<table id="table_tw1_frx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_glide\_lookup\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_fields**

</td></tr><tr><td>

Additional Fields

</td><td>

-   **target\_table**
-   **glide\_matching\_fields** \(string\): Comma-separated list of column names in the target table. For each input field in **source\_sys\_rte\_eb\_fields**, there must be an equal number of values in **glide\_matching\_fields**
-   **glide\_target\_fields** \(string\): Comma-separated list of column names in the target table. For each target field in **target\_sys\_rte\_eb\_fields**, there must be an equal number of values in **glide\_target\_fields**.

</td></tr></tbody>
</table><table id="table_jlm_xw1_bmb"><thead><tr><th>

Example

</th><th>

 

</th></tr></thead><tbody><tr><td>

Input

</td><td>

-   Input Field 1: 100 South Charles Street, Baltimore
-   Input Field 2: MD

</td></tr><tr><td>

Additional Fields

</td><td>

-   Target Table: Location \(cmn\_location\)
-   Glide Matching Fields: street,state
-   Glide Target Fields: sys\_id

</td></tr><tr><td>

Result

</td><td>

Output Field 1: 25ab9c4d0a0a0bb300f7dabdc0ca7c1c

</td></tr></tbody>
</table>### Min/Max

Sets the target field to either the maximum or minimum of the values from all input fields.

<table id="table_fpb_frx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_min\_max\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Additional Fields

</td><td>

-   **data\_type** \(choice list &lt;STRING,NUMERIC,DATE&gt;\)
-   **min\_max** \(choice list &lt;MIN,MAX&gt;\)

</td></tr></tbody>
</table><table id="table_pm1_jsf_hlb"><thead><tr><th>

Example

</th><th>

 

</th></tr></thead><tbody><tr><td>

Input

</td><td>

“2”, “-1”, “0”

</td></tr><tr><td>

Additional Fields

</td><td>

-   **data\_type** = NUMERIC
-   **min\_max** = MAX

</td></tr><tr><td>

Result

</td><td>

“2”

</td></tr></tbody>
</table><table id="table_knx_jsf_hlb"><thead><tr><th>

Example

</th><th>

 

</th></tr></thead><tbody><tr><td>

Input

</td><td>

“a”, “b”

</td></tr><tr><td>

Additional Fields

</td><td>

-   **data\_type** = STRING
-   **min\_max** = MAX

</td></tr><tr><td>

Result

</td><td>

“b”

</td></tr></tbody>
</table><table id="table_kl4_psf_hlb"><thead><tr><th>

Example

</th><th>

 

</th></tr></thead><tbody><tr><td>

Input

</td><td>

“2”, “-1”, “0”

</td></tr><tr><td>

Additional Fields

</td><td>

-   **data\_type** = NUMERIC
-   **min\_max** = MIN

</td></tr><tr><td>

Result

</td><td>

“-1”

</td></tr></tbody>
</table><table id="table_ll4_psf_hlb"><thead><tr><th>

Example

</th><th>

 

</th></tr></thead><tbody><tr><td>

Input

</td><td>

“a”, “b”

</td></tr><tr><td>

Additional Fields

</td><td>

-   **data\_type** = STRING
-   **min\_max** = MIN

</td></tr><tr><td>

Result

</td><td>

“a”

</td></tr></tbody>
</table>### Multiple Input Script

Runs a script with multiple inputs, setting the **target\_field** == output for that script.

Each source field is available inside of the ‘batch’ variable as JavScript fields. The name of the JavaScript field is the field attribute of the entity field \(looking at **sys\_rte\_eb\_field.field**, not **sys\_rte\_eb\_field.name**\).

<table id="table_shc_frx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_multi\_in\_script\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Additional Fields

</td><td>

-   **script** \(script\)
-   **use\_unique\_input\_sets** \(boolean\): When **true**, only unique input values are included in the data batch for IRE processing. Otherwise, all input object’s field values are included.

</td></tr></tbody>
</table>Example for using **use\_unique\_input\_sets**, with a script function that takes **record\_type** and **operating\_system** as input and returns **record\_with\_os**:

|Record|record\_type|operating\_system|record\_with\_os|
|------|------------|-----------------|----------------|
|1|computer|Windows XP| |
|2|computer|Linux| |
|3|computer|Windows XP| |

If **use\_unique\_inputs\_sets** is set to **true**, then the script processes only two values \(computer + Windows XP and computer + Linux\). If **use\_unique\_inputs\_sets** is set to **false**, then each of the three values is individually processed \(computer + Windows XP, computer + Linux, and computer + Windows XP\).

Sample script:

```
            (function(batch, output) { 
                for (var i = 0; i < batch.length; i++) { 
                        // batch[i] is the unique set of inputs/individual record 
                        // batch[i].<field> gives access to the field value 
                        var in0 = gs.nil(batch[i].record_type) ? '' : batch[i].record_type;
                        var in1 = gs.nil(batch[i].operating_system) ? '' : batch[i].operating_system;
                        // output[i] is the output for the specific combination of inputs/individual record 
                        output[i] = in0 + "_" + in1; 
                    } 
                } 
            })(batch, output);
```

Sample script:

```
            /* Example Script
             // In this example the script input fields are 'input_field_1', 'input_field_2' - replace these with the fields used as script inputs // There is a static field 'input' that has all the input field values concatenated with a '|' (function(batch, output) {
                 for (var i = 0; i < batch.length; i++) {
           
                     //step1: access the input variables
                     var a = batch[i].input_field_1; //Value of the first source field.
                     var b = batch[i].input_field_2; //Value of the second source field.
             
                     //step2: Your script/code goes here.
                     var c = a + b;
           
                     //step3: set the output for each elements
                     output[i] = b;
                 }
           
             })(batch, output);
            */
```

### Rexeg Replace

Replaces each substring of the incoming string that matches the specified **match\_regex**, with the specified **replacement\_regex** string value.

<table id="table_t1d_frx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_regex\_replace\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Additional Fields

</td><td>

-   **match\_regex** \(string, regular expression\)
-   **replacement\_regex** \(string\)

</td></tr></tbody>
</table><table id="table_qn3_xsf_hlb"><thead><tr><th>

Example

</th><th>

 

</th></tr></thead><tbody><tr><td>

Input

</td><td>

“String&amp;With\(Special\)$Characters”

</td></tr><tr><td>

Additional Fields

</td><td>

-   **match\_regex** = “\[^0-9a-zA-Z\]+”
-   **replacement\_regex** = “ ”

</td></tr><tr><td>

Result

</td><td>

“String With Special Characters”

</td></tr></tbody>
</table>### Replace

Replaces each substring in the incoming string that matches the specified **match\_string**, with the **replacement\_string** string value.

<table id="table_gsd_frx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_replace\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Additional Fields

</td><td>

-   **match\_string** \(string\)
-   **replacement\_string** \(string\)

</td></tr></tbody>
</table><table id="table_czw_1tf_hlb"><thead><tr><th>

Example

</th><th>

 

</th></tr></thead><tbody><tr><td>

Input

</td><td>

“Original String”

</td></tr><tr><td>

Additional Fields

</td><td>

-   **match\_string** = “Original”
-   **replacement\_string** = “Replacement”

</td></tr><tr><td>

Result

</td><td>

“Replacement String”

</td></tr></tbody>
</table>### Round Numeric

Rounds the number value to the nearest whole number. Non-numbers are truncated.

|Details| |
|-------|---|
|Table|sys\_rte\_eb\_round\_numeric\_operation|
|Input fields|**source\_sys\_rte\_eb\_field**|
|Output field|**target\_sys\_rte\_eb\_field**|

|Example| |
|-------|---|
|Input|“1.5”|
|Result|"2"|

|Example| |
|-------|---|
|Input|“1.4”|
|Result|"1"|

|Example| |
|-------|---|
|Input|“i’m a string”|
|Result|""|

### Script

Runs a script with input, setting the target\_field == output for that script.

This transform has been superseded by the Multi Input Script transform and is included for backwards compatibility with existing configurations.

<table id="table_u2f_frx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_script\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Additional Fields

</td><td>

-   **script** \(script\)
-   **use\_unique\_input\_sets** \(boolean\): When **true**, only unique input values are included in the data batch for IRE processing. Otherwise, all input object’s field values are included. For an example and for more details, see the Multiple Input Script transform.

</td></tr></tbody>
</table>The source field is included in the ‘batch’ variable as the JavaScript field ‘input’.

```
          (function(batch, output) { 
                for (var i = 0; i < batch.length; i++) { 
                        // batch[i] is the unique set of inputs/individual record 
                        // batch[i].input gives access to the field value 
                        var in0 = gs.nil(batch[i].input) ? '' : batch[i].input; 
                        // output[i] is the output for the specific combination of inputs/individual record 
                        output[i] = in0 + " modified by script”; 
                    } 
                } 
            })(batch, output); 
```

Example:

```
/* Example Script
 (function(batch, output) {
     for (var i = 0; i < batch.length; i++) {
         //step1: access the input variables
         var a = batch[i].input; //Value of the source field.
 
         //step2: Your script/code goes here.
         var b = a + 1;
         //step3: set the output for each elements
         output[i] = b;
     }
 })(batch, output);
*/ 
```

### Set

Sets the target field’s value to the string specified in **set\_value**.

<table id="table_jqg_frx_glb"><thead><tr><th>

Details

</th><th align="center">

 

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sys\_rte\_eb\_set\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field**

</td></tr><tr><td>

Additional Fields

</td><td>

-   **set\_value** \(string\)
-   **overwrite\_existing\_value** \(optional, boolean\): When **true**, the current value of the target field is overwritten. Otherwise, a non-empty value isn't replaced.

</td></tr></tbody>
</table>### Split

Splits the source field’s value on the **splitting\_string** and assigns each resulting item from the split to the **target\_sys\_rte\_eb\_fields**, in order.

|Details| |
|-------|---|
|Table|sys\_rte\_eb\_split\_operation|
|Input fields|**source\_sys\_rte\_eb\_field**|
|Output field|**target\_sys\_rte\_eb\_fields**|
|Additional Fields|**splitting\_string** \(string\)|

|Example| |
|-------|---|
|Input|“value1\|\|value2\|\|value3”, with **target\_sys\_rte\_eb\_fields** \{target1,target2,target3\}|
|Additional Fields|**splitting\_string** = ”\|\|”|
|Result|target1 : value1, target2 : value2, target3 : value3|

|Example| |
|-------|---|
|Input|“value1\|\|value2\|\|value3”, with **target\_sys\_rte\_eb\_fields** \{target1\}|
|Additional Fields|**splitting\_string** = ”\|\|”|
|Result|target1 : value1|

|Example| |
|-------|---|
|Input|“value1”, with **target\_sys\_rte\_eb\_fields** \{target1,target2,target3\}|
|Additional Fields|**splitting\_string** = ”\|\|”|
|Result|target1 : value1, target2 : &lt;null&gt;, target3 : &lt;null&gt;|

### Trim

Trims leading and trailing whitespace from the **source\_sys\_rte\_eb\_field** value and assigns the result to the**target\_sys\_rte\_eb\_field**. This transform is equivalent to a Java String.trim\(\).

|Details| |
|-------|---|
|Table|sys\_rte\_eb\_trim\_operation|
|Input fields|**source\_sys\_rte\_eb\_field**|
|Output field|**target\_sys\_rte\_eb\_field**|

|Example| |
|-------|---|
|Input|“ value 1 ”|
|Result|“value 1”|

### Uppercase

Uppercases the **source\_sys\_rte\_eb\_field** value and assigns the result to **target\_sys\_rte\_eb\_field**.

|Details| |
|-------|---|
|Table|sys\_rte\_eb\_upper\_case\_operation|
|Input fields|**source\_sys\_rte\_eb\_field**|
|Output field|**target\_sys\_rte\_eb\_field**|

|Example| |
|-------|---|
|Input|“value1”|
|Result|“VALUE1”|

### Uppercase Trim

Combines both the Uppercase and the Trim transforms.

|Details| |
|-------|---|
|Table|sys\_rte\_eb\_upper\_case\_trim\_operation|
|Input fields|**source\_sys\_rte\_eb\_field**|
|Output field|**target\_sys\_rte\_eb\_field**|

|Example| |
|-------|---|
|Input|“ value1 ”|
|Result|“VALUE1”|

