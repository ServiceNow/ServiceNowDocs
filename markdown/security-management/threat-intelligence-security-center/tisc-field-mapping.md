---
title: Configure Custom Field Mapping
description: Field Mapping allows you to configure how each field in a data feed such as Text, CSV or JSON is interpreted and assigned to the corresponding observable.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-21"
reading_time_minutes: 4
breadcrumb: [Threat Intelligence Feeds, Integrate Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
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

    ![TISC - Field Mapping Adding Sample Data.](../image/tisc-field-map-sample-data.png)

11. Select **Next** to configure the field mapping.

12. Select **Set a delimiter for parsing data** option from the drop down list.

    When working with Text feeds, the delimiter is essential for correctly parsing the data into individual fields.

    In this scenario, the text feed uses the pipe operator \(\|\) as the delimiter which separates each value in the sample text data into distinct columns. Correctly identifying and applying this delimiter is essential to ensure accurate field mapping and successful data ingestion.

    **Note:** For CSV feeds comma \(,\) is the default delimiter, and JSON feeds doesn't require any delimiter.

13. Select **Update delimiter**.

    The options to add fields for field mapping are displayed.

14. Proceed to add the field mapping by selecting the appropriate values from the drop down list.

    ![TISC Field Mapping Data Delimiter](../image/tisc-field-mapping-data-delimiter.png)

15. Use the **Transform Script** to transform and normalize the input values before mapping them to observables.

    1.  Select **Enable/disable transform script** icon to configure the script.

        The Configure script for source field dialogue box is displayed.

    2.  Select **Enable Transform Script** check box on the **Configure script for source field** dialogue box.

    3.  Add or modify the script.

        For example, if your input field contains values such as low, medium, or high and you want to map these values to numerical confidence levels \(between 0–100\), then you can use Transform Script to convert the input value and map it to the **Confidence** field of the observable.

        ![TISC Field Mapping Transform Script](../image/tisc-field-mapping-transform-script.png)

    4.  Select **Save** to save the script to get the updated target value.

    5.  Close **Configure script for source field** dialogue box and proceed with the next step.

16. Select **Next** to proceed to preview the field mappings in the **Preview** section.

    ![TISC - Field Mapping preview sample data.](../image/tisc-field-mapping-preview-data.png)

17. Preview the sample field mapping and select **Save**.

    A confirmation message is displayed indicating that the field mapping is saved successfully.

    As part of sample field mapping, the application automatically identifies the observable type \(such as IP address v4 and so on\) that the user has mapped from the sample data. This mechanism streamlines the mapping process and ensures the appropriate observable types are assigned based on the input.

    **Important:** Field Mapping Integration Run: Any integration run performed for this feed type will use the saved field mapping configuration. This ensures that incoming data is consistently parsed and mapped to the correct observable attributes based on the structure defined during the configuration.

    **Note:** Select **Edit Field Mapping** to edit and make any necessary changes to the field mapping if required. An alert message is displayed to confirm if you want to proceed with editing. Acknowledge the prompt and select **Yes** to continue. Make the necessary changes to the field mappings using the updated sample data and save the changes.

    Any edits made to the field mapping will be applied to the future integration runs for this feed.

    Always verify the sample data after changes to ensure correct parsing before running the integration.


**Parent Topic:**[Threat Intelligence Feeds](../concept/threat-intelligence-feeds.md)

