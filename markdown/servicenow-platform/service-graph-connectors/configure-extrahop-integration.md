---
title: Configure Service Graph Connector for ExtraHop
description: Set up a REST message and scheduled jobs to import ExtraHop data into your CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [ExtraHop, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for ExtraHop

Set up a REST message and scheduled jobs to import ExtraHop data into your CMDB.

## Before you begin

**Important:** ServiceNow hosted Service Graph Connector for ExtraHop is now deprecated and no longer supported or available for new activation. ExtraHop hosted Service Graph Connector for ExtraHop provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=australia&pubname=australia-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md).
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).
-   ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   MID Server that is installed on Linux or Windows, unless the ExtraHop appliance is publicly accessible.
-   ExtraHop Discover appliance with firmware version 7.2 or later, with a user account that has unlimited privileges.
-   To connect to the ExtraHop application, configure an API key. For more information, see [ExtraHop REST API Guide](https://docs.extrahop.com/8.1/rest-api-guide/), specifically, see the "ExtraHop API requirements" section.

Roles required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connector ExtraHop** &gt; **Setup**.

2.  On the Getting started page, click **Get Started**.

3.  On the Service Graph Connector for the ExtraHop page, in the Configure REST message section, select the task **Configure ExtraHop REST message**.

4.  Configure a REST message to use when sending requests to the ExtraHop API.

    1.  On the next page, in the Configure ExtraHop REST message task section, click **Configure**.

    2.  On the form, fill in the fields.

<table id="table_g1x_pgp_wlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for this REST Message. This field is automatically set.

</td></tr><tr><td>

Endpoint

</td><td>

URL to the web service API endpoint. Set the field to a base URL. For example, `https://myextrahop.com`. **Note:** Updating the Endpoint base URL also updates the base URLs for all HTTP methods that are associated with the ExtraHop REST message. In the **HTTP Request** tab, update the Authorization header to use your API key in the **Value** field.

</td></tr><tr><td>

Description

</td><td>

Description for this REST Message. This field is automatically set.

</td></tr><tr><td>

Application

</td><td>

Application that contains this message. The field is automatically set.

</td></tr><tr><td>

Authentication type

</td><td>

Type of authentication to apply to HTTP requests. The field is automatically set.

</td></tr><tr><td>

Use mutual authentication

</td><td>

Option to use multiple authentication by authenticating HTTP requests. Mutual authentication cannot be used with a MID Server.

</td></tr></tbody>
</table>    3.  Click **Update** if necessary.

    4.  In the Configure ExtraHop REST message task section, click **Mark as Complete**.

5.  Test the connection to the ExtraHop Computer API.

    1.  In the Test Computer connection task section, click **Configure**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |:----|:----------|
        |Name|Unique identifier for this HTTP method. This field is automatically set.|
        |Endpoint|URL to the web service API endpoint|
        |Use MID Server|MID Server that sends this HTTP request. Using a MID Server is not compatible with mutual authentication.|
        |REST Message|REST message record that this method is based on. This field is automatically set.|
        |HTTP method|HTTP method that is implemented by this method. This field is automatically set.|
        |Application|Application that contains this method. This field is automatically set.|
        |Authentication type|Type of authentication to apply to HTTP requests.|
        |Use mutual authentication|Option to use multiple authentication by authenticating HTTP requests. Mutual authentication cannot be used with a MID Server.|

    3.  Select the **HTTP Request** tab and fill out the **Use MID Server** field.

    4.  Click the **Authentication** tab and then click the **Test** related link.

        Testing the connection takes a few moments. When the test is complete, the page is refreshed and shows the test results.

    5.  Select **Mark as Complete**.

        **Note:** The connection is successful if the **HTTP Status** field is set to **200**. If there are any errors in the **Error Message** field, then the connection failed and further troubleshooting is required.

    6.  Click **Update** if necessary.

    7.  In the Test Computer connection task section, click **Mark as Complete**.

6.  Test the connection to the ExtraHop Network Activity Create API.

    1.  In the Test Network Activity Create connection task section, click **Configure**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |:----|:----------|
        |Name|Unique identifier for this HTTP method.|
        |Endpoint|URL to the web service API endpoint|
        |Use MID Server|MID Server that sends this HTTP request. Using a MID Server is not compatible with mutual authentication.|
        |REST Message|REST message that this method is based on. This field is automatically set.|
        |HTTP method|HTTP method that is implemented by this method. This field is automatically set.|
        |Application|Application that contains this record. This field is automatically set.|
        |Authentication type|Type of authentication to apply to HTTP requests. This field is automatically set.|
        |Use mutual authentication|Option to use multiple authentication by authenticating HTTP requests. Mutual authentication cannot be used with a MID Server.|

    3.  Click the **Authentication** tab and then click the **Test** related link.

        Testing the connection takes a few moments. When the test is complete, the page is refreshed and shows the test results.

    4.  Select **Mark as Complete**.

        **Note:** The connection is successful if the **HTTP Status** field is set to **200**. If there are any errors in the **Error Message** field, then the connection failed and further troubleshooting is required.

    5.  Click **Update** if necessary.

    6.  In the Test Network Activity Create connection task section, click **Mark as Complete**.

7.  Set up the scheduled import jobs.

    1.  On the Service Graph Connector for ExtraHop page, in the Set up scheduled import jobs section, select the task **Configure Computer scheduled job**.

    2.  In the Configure Computer scheduled job task section, click **Configure**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |:----|:----------|
        |Name|Name of the scheduled job.|
        |Data source|Data source record that defines the data to import.|
        |Run as|Option to run the scheduled job with the credentials of the specified user.|
        |Active|Option to activate the scheduled job. Select this option.|
        |Concurrent Import|Function that loads the data from multiple import sets. The function then processes and transforms the data concurrently.|
        |Partition Method|Partition method for the concurrent import set.|
        |Partition Size|Import set size for early scheduling.|
        |Execute pre-import script|Option to specify a script to run before the import is performed.|
        |Execute post-import script|Option to specify a script to run after the import is performed.|
        |Application|Application that contains this scheduled job.|
        |Run|Frequency of running the import.|
        |Conditional|Conditions under which this job is executed.|

    4.  Click **Update** if necessary.

    5.  In the Configure Computer scheduled job task section, click **Mark as Complete**.

8.  Configure the Network Activity scheduled job.

    1.  On the Service Graph Connector for ExtraHop page, in the Set up scheduled import jobs section, select the task **Configure Network Activity scheduled job**.

    2.  In the Configure Network Activity scheduled job task section, click **Configure**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |:----|:----------|
        |Name|Name of the scheduled job.|
        |Data source|Data source record that defines the data to import.|
        |Run as|Option to run the scheduled job with the credentials of the specified user.|
        |Active|Option to activate the scheduled job. Select this option.|
        |Concurrent Import|Function that loads the data from multiple import sets. The function then processes and transforms the data concurrently.|
        |Partition Method|Partition method for the concurrent import set.|
        |Partition Size|Import set size for early scheduling.|
        |Execute pre-import script|Option to specify a script to run before the import is performed.|
        |Execute post-import script|Option to specify a script to run after the import is performed.|
        |Application|Application that contains this scheduled job.|
        |Run|Frequency of running the import.|
        |Conditional|Conditions under which this job is executed.|

    4.  Click **Update** if necessary then **Mark as Complete**.


