---
title: Configure Custom Field Mapping
description: Field Mapping allows you to configure how each field in a data feed such as Text, CSV or JSON is interpreted and assigned to the corresponding observable.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 5
breadcrumb: [Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure Custom Field Mapping

Field Mapping allows you to configure how each field in a data feed such as Text, CSV or JSON is interpreted and assigned to the corresponding observable.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations**.

2.  Select **Threat Intel Feeds** &gt; **All Feeds** &gt; **Text**.

3.  Select **Configure new source**.

4.  Fill in the text feed form details as required.

    For more information see, [Configure a new threat intelligence feed](tisc-new-data-source.md).

5.  On the new form view, drill down to **Data Parsing Mechanism** field under the **Configuration** section.

    For more information on Data Parsing Mechanism, see [Configure a new threat intelligence feed](tisc-new-data-source.md).

6.  Select **Custom Field Mapping** option.

7.  Navigate to the **Field Mapping** section.

8.  Select **Configure** to add the field mapping for the new data source.

    This section involves three steps such as adding sample data, field mapping, and previewing the mapped sample records.

9.  To add the sample data, select **Load Sample Data**.

    This displays the sample data from the selected option, the application displays only the relevant data rows and lines that begin with `#` are excluded from the sample data. The comment identifiers can be modified with the system property: `sn_sec_tisc.feed_comment_identifiers`.

    The application will fetch a sample of the incoming data either from a sample file \(such as .txt, .csv, or .json\) or directly from the configured feed URL \(the feed URL and credentials entered in the **Details** section\). This allows you to preview the structure and contents of the data before defining field mappings.

10. Select either **Upload a sample file** or **Feed data from feed URL**.

    This sample data will fetch the first ten records by default, this total number of records to be retrieved can be modified with the system property `sn_sec_tisc.feed_field_mapping_sample_count`.

    The list view displays a code editor preserving the original structure and formatting of raw data.

    ![TISC - Field Mapping Adding Sample Data.](../image/tisc-field-map-sample-data.png)

11. Select **Next** to configure the field mapping.

12. Select **Set a delimiter for parsing data** option from the drop down list.

    When working with Text feeds, the delimiter is essential for correctly parsing the data into individual fields.

    In this scenario, the text feed uses the pipe operator \(\|\) as the delimiter which separates each value in the sample text data into distinct columns. Correctly identifying and applying this delimiter is essential to ensure accurate field mapping and successful data ingestion.

    Regular expressions\(RegEx\) are also supported as delimiters for the text feed, providing additional flexibility when parsing complex feed data and not support for the JSON and CSV feeds.

    **Note:** For CSV feeds comma \(,\) is the default delimiter and JSON feeds doesn't require any delimiter.

13. Select **Update delimiter**.

    The options to add fields for field mapping are displayed.

14. Proceed to add the field mapping by selecting the appropriate values from the drop down list.

    ![TISC Field Mapping Data Delimiter](../image/tisc-field-mapping-data-delimiter.png)

15. Use the **Transform Script** to transform and normalize the input values before mapping them to observables.

    You can map the same source column \(for example, column 2\) multiple times such as to the **Additional Context** field using a dedicated script handler.

    **Important:**

    -   Multiple source field mapped with the same target observable fields of type `string`. For a reference list of string-type fields, see the `sn_sec_tisc_observable_source` table.
    -   The **Observable fields** type such as **Additional Context**, **Author**, and **Description** allow multiple field mappings. Review and update the mappings as needed.
    -   The same source field can be mapped to multiple target fields without any limitations.
    Transform scripts can be applied to customize how data is processed and enriched during mapping.

    1.  Select **Enable/disable transform script** icon to configure the script.

        The Configure script for source field dialogue box is displayed.

    2.  Select **Enable Transform Script** check box on the **Configure script for source field** dialogue box.

    3.  Add or modify the script.

        For example, if your input field contains values such as low, medium, or high and you want to map these values to numerical confidence levels \(between 0–100\), then you can use **Transform Script** to convert the input value and map it to the **Confidence** field of the observable.

        For example, if your input field contains a string value and you want to map these values to a string type as **Additional Context \(observable type\)**, then you can either use the **Transform Script** to input the value or without the **Transform Script** to map it to the **Additional Context** field of the observable.

        **Note:** Each individual mapping record supports its own script, allowing users to define custom transformation logic for every mapping.

        ![TISC Field Mapping Transform Script](../image/tisc-field-mapping-transform-script.png)

    4.  Select **Save** to save the script to get the updated target value.

    5.  Close **Configure script for source field** dialogue box and proceed with the next step.

        ![Field level mapping.](../image/tisc-field-script-mapping.png)

16. Select **Next** to proceed to preview the field mappings in the **Preview** section.

    ![TISC - Field Mapping preview sample data.](../image/tisc-field-mapping-preview-data.png)

17. Preview the sample field mapping and select **Save**.

    A confirmation message is displayed indicating that the field mapping is saved successfully.

    As part of sample field mapping, the application automatically identifies the observable type \(such as IP address v4 and so on\) that the user has mapped from the sample data. This mechanism streamlines the mapping process and ensures the appropriate observable types are assigned based on the input.

    If multiple source fields are mapped to the same **Observable field** such as **Additional Context**, then after feed ingestion the values will appear in the respective mapped field \(which is the **Additional Context**\), each separated by a new line. The following is the sample screen shot of the observable column displayed in the new line.

    ![Observable source column - Additional Context](../image/tisc-field-map-config-obs-column.png)

    **Important:** Field Mapping Integration Run: Any integration run performed for this feed type will use the saved field mapping configuration. This ensures that incoming data is consistently parsed and mapped to the correct observable attributes based on the structure defined during the configuration.

    **Note:** Select **Edit Field Mapping** to edit and make any necessary changes to the field mapping if required. An alert message is displayed to confirm if you want to proceed with editing. Acknowledge the prompt and select **Yes** to continue. Make the necessary changes to the field mappings using the updated sample data and save the changes.

    Any edits made to the field mapping will be applied to the future integration runs for this feed.

    Always verify the sample data after changes to ensure correct parsing before running the integration.


**Parent Topic:**[Threat Intelligence Feeds](../concept/threat-intelligence-feeds.md)

