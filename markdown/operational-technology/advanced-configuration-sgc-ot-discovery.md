---
title: Use advanced configurations
description: Use the advanced configuration for the Service Graph Connector for ServiceNow OT Discovery to set up an asset extension points, a class calculator extension points, and a configuration item \(CI\) naming strategy extension points.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connector for ServiceNow Operational Technology\(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Use advanced configurations

Use the advanced configuration for the Service Graph Connector for ServiceNow OT Discovery to set up an asset extension points, a class calculator extension points, and a configuration item \(CI\) naming strategy extension points.

## Before you begin

Role required: admin

## Procedure

1.  Set up an asset extension point.

    Before being transformed by the Robust Transformer \(RTE\) and the Integration Hub ETL, the assets from the OT Discovery API are flattened into a standard format. If you want to include additional custom attributes into the flattened asset, you can choose to use the Asset Extension Point script. Once the extension point is implemented, you can transform and map the additional custom attributes using the Integration Hub ETL.

    1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **OT Discovery** &gt; **Extension Points**

    2.  Select the **x\_snc\_mis\_sec\_sgc.SGMissionSecureAssetExtension** record.

    3.  In the Related Links section, select **Create implementation**

    4.  In the script, update the process function to include the desired additional attributes using Javascript.

        The following image is an example of a `custom_attribute` being added to the flattened asset.

        ![A custom attribute added to the script include](../../sgc-ot-discovery/image/asset-extension-point-example-sgc-msi.jpg)

    5.  Once the script is complete, validate the data by running a test load of the Data Source.

    6.  After you run the test load, navigate to **All** &gt; **System Import Sets** &gt; **Staging SG-OT Discovery Asset**.

    7.  Validate that the Data column contains the `custom_attribute` that you added in step 1d.

        If the custom attribute doesn't appear, compare the `api_data` to the data to correct the issue with your code.

    8.  Navigate to **Configuration** &gt; **IntegrationHub ETL**.

    9.  Under CMDB Application SG-OT Discovery, select the **SG-OT Discovery Asset** record.

    10. Under **1. Specify Basic Details**, select **Import Source Data and Provide Basic Details**.

    11. Ensure that Integration Hub ETL is using a sample import with the **custom\_attribute** from the previous step or scroll down and use the the **Auto-pull a new import set** option.

    12. Select **Save** and **Mark as Complete** to retrieve the import set.

        **Note:** You may see error messages when navigating back to the ETL Transform Map Assistant. You can ignore these messages.

    13. Use **Preview and Prepare Data** and select **CMDB Classes to Map Source Data** to transform and map the custom\_attribute as desired.

2.  Set up a class calculator extension point.

    During transformation, classification of assets from the OT Discovery API is calculated based on the OT Discovery category and, optionally, the Network type of the Site \(OT orIT\) using the OT Discovery Classification Settings. An extension point is provided for additional advanced configuration which overrides the classification setting.

    1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **OT Discovery** &gt; **Extension Points**.

    2.  Select the **x\_snc\_mis\_sec\_sgc. SGMissionSecureClassCalculatorOverride** record.

    3.  In the Related Links section, select **Create implementation**.

    4.  In the script, update the process function as desired.

        The following image shows an example of an updated script.

        ![Updated script include for the class calculator extension point](../../sgc-ot-discovery/image/class-calculator-example-sgc-msi.jpg)

3.  Set up a Configuration Item \(CI\) Naming Strategy extension point.

    The Service Graph Connector for OT Discovery comes with **JustNameFallbackIPAddressAndNetworkZone**, which is a default CI Naming Strategy. If you want to name the CIs differently, you can configure additional CI Naming Strategies using the extension point.

    1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **OT Discovery** &gt; **Extension Points**

    2.  Select the **x\_snc\_mis\_sec\_sgc. SGMissionSecureCINameCalculation** record.

    3.  In the Related Links section, select **Create implementation**.

    4.  In the script include, update the following fields.

        -   Update the **Name** field to an appropriate name for the CI Naming Strategy.

            You must start the name with **SGOTDiscoveryCINameCalculation** and add the rest of the name using camel-casing with no spaces or special characters. For example, `SGOTDiscoveryCINameCalculationAppendMAC`.

        -   In the **Script** field, update the `calculateCIName` function as needed.
    5.  Navigate to **Service Graph Connectors** &gt; **OT Discovery** &gt; **Classification Settings**.

    6.  Select the record that uses the new naming strategy.

    7.  Change the **CI naming strategy** field to the new CI Naming Strategy.

    8.  Repeat needed steps for any additional classification settings that should use your CI Naming Strategy.


