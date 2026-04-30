---
title: Configure Service Graph Connector for Nokia Altiplano
description: This document explains how to configure the Service Graph Connector for Nokia Altiplano using Guided setup to integrate network resource data from the Nokia Altiplano Access Controller \(REST API\) into the ServiceNow CMDB. It includes steps for setup, authentication, and scheduling to confirm accurate integration of network data.This procedure is applicable for initial setup of the Nokia Altiplano.Add Second instance of a Nokia Altiplano and subsequent instances.
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Telecom Discovery using Service Graph Connectors \(SGC\), Exploring Telecom Discovery, Telecom Discovery, TSOM Visibility, Telecommunications Service Operations Management]
---

# Configure Service Graph Connector for Nokia Altiplano

This document explains how to configure the Service Graph Connector for Nokia Altiplano using Guided setup to integrate network resource data from the Nokia Altiplano Access Controller \(REST API\) into the ServiceNow CMDB. It includes steps for setup, authentication, and scheduling to confirm accurate integration of network data.

To use Service Graph Connector for Nokia Altiplano, you need a subscription to TSOM.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Dependencies and requirements

-   TSOM Visibility plugin \(**sn\_tsom\_core**\)
-   Discovery Core plugin \(**com.snc.discovery.core**\), which is automatically installed by Discovery.
-   ITOM Discovery License plugin \(**com.snc.itom.discovery.license**\). You must activate this plugin.
-   ITOM Licensing plugin \(**com.snc.itom.license**\).

    For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

-   For development environment only - IntegrationHub ETL \(**sn\_int\_studio**\).
-   Nokia Altiplano Platform \(access to its REST northbound API\).

Roles required: admin

## TSOM Visibility Installation Disclaimer

See [TSOM Visibility Installation Disclaimer](tsom-visibility.md#section_wn4_2fk_b2c), for important information and requirements related to the installation process.

**Parent Topic:**[Telecom Discovery using Service Graph Connectors \(SGC\)](telecom-discovery-using-service-graph-connector.md)

## Initial Setup procedure

This procedure is applicable for initial setup of the Nokia Altiplano.

### Before you begin

Role required: admin

Change the application scope to ‘Service Graph Connector for Nokia Altiplano’ by selecting the ![](../../../reuse/icons/product-icons/globe-outline-24.svg), searching for Nokia Altiplano, and selecting it.

![application scope.](../images/telecom-initial-setup.png)

### Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Nokia Altiplano** &gt; **Setup**.

2.  On the Getting started page, select **Get Started**.

3.  Configure MID Server:

    1.  Select **Configure**.

    2.  If a MID Server has been configured, set all to **Mark as Complete**.

        For more information on how to install and configure MID Server, see [Configuring MID Server](https://www.servicenow.com/docs/access?context=configure-mid-server&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

4.  Configure Connectivity:

    1.  Select **Get Started**.

    2.  Configure aliases for the connections and credentials:

        1.  Select **Configure**.
        2.  In the Name filed, specify the allies name.
        3.  Leave the rest of the fields as default, select **Submit** and then **Mark as Complete**.

            ![connections and credentials.](../images/telecom-configure-connectivity.png)

        This enables using the connection by name rather than directly, enabling the collector to extract all active aliases from the CMDB and start performing data collection on the HTTP connection bound to it.

    3.  Create the credentials to access the Nokia Altiplano Controller:

        1.  Select **Configure**.

        2.  In the **Name** field, specify your Nokia Altiplano instance user name.

        3.  In the **Password** field, specify your Nokia Altiplano instance password.

            **Note:**

            Other authentication fields may be required depending on the authentication methods used in your Nokia Altiplano instance. By default, we use [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) \(as part of the Guided setup\).

        4.  Leave the rest of the fields as default, select **Submit** and then **Mark as Complete**.

        ![basic auth credentials.](../images/telecom-create-credentials.png)

    4.  Create HTTP Connection:

        1.  Select **Configure**.

        2.  In the **Name** filed, specify the HTTP connection name.

        3.  In the **Credentials** field, select the magnifying glass icon and select the credential defined in section 5.b

        4.  In the **Connection alias** field, select the ![](../../../reuse/icons/product-icons/magnifying-glass-fill-24.svg) icon and select the Connection allies defined in section 5.a

        5.  In the Connection URL field, specify the Nokia Altiplano URL.

        6.  Check the **Use MID Server** check box and select the specific MID Server or MID Server Cluster to run discovery from.

        7.  Leave the rest of the fields as default, select **Submit** and then **Mark as Complete**.

        ![http connection.](../images/telecom-create-http-connection.png)

5.  Configure Data Collection Schedule:

    1.  Select **Get Started**.

        1.  Select **Configure**.
        2.  In the **Name** filed, specify the scheduler name.
        3.  In the **Data source** field, select the ![](../../../reuse/icons/product-icons/magnifying-glass-fill-24.svg) icon and select a data source for OLT discovery:
            -   **SG Altiplano OLT for All**- Select this option for all aliases \(instances\) of Nokia Altiplano.
            -   **SG Altiplano OLT \[ALIAS\_NAME\]**- Select this option for the specific alias of an Altiplano instance.
        4.  Check the **Active** check box to activate.

            Specify when do you want this schedule to run \(daily, weekly, monthly. periodically, after parent run, once\).

        5.  You can run it now by selecting the **Execute Now**.
        6.  Leave the rest of the fields as default, select **Update**, and then **Mark as Complete**.
        ![scheduled data import.](../images/telecom-scheduled-data-import.png)

    2.  Schedule Data Collection for ONU:

        1.  Select **Configure**.
        2.  In the **Name** field, specify the scheduler name.
        3.  In the **Data source** field, select the ![](../../../reuse/icons/product-icons/magnifying-glass-fill-24.svg) and select a data source for ONU discovery:
            -   **SG Altiplano ONU for All**- Select this option for all aliases \(instances\) of Nokia Altiplano.
            -   **SG Altiplano ONU \[ALIAS\_NAME\]**- Select this option for the specific alias of an Altiplano instance.
        4.  Check the **Active** check box to activate.

            **Note:** Specify when do you want this schedule to run \(daily, weekly, monthly. periodically, after parent run, once\).

        5.  You can run it now by selecting the **Execute Now**.
        6.  Leave the rest of the fields as default, press **Update** then **Mark as Complete**.
6.  Test the connection by using the **Test Load 20 Records** related link.

    This step tests the selected data source and confirms that the data is loaded into the staging table. A successful connection indicates that the selected Nokia Altiplano data source has connected successfully. Perform this action for both **SG-Altiplano OLT for all** and **SG-Altiplano ONU for all** data sources, as well as for any other data sources you have created.

    1.  Navigate to **Service Graph Connectors** &gt; **Nokia Altiplano** &gt; **Data Sources**.

7.  Select the desired Data Source.

8.  On the Data Source form, under Related Links, select Test Load 20 Records.

9.  Wait for the test result State to be Complete with a Completion code of Success.

    ![test result.](../images/test-connection.png)


## Multi-Instance setup

Add Second instance of a Nokia Altiplano and subsequent instances.

### Before you begin

Role required: admin

Change the application scope to Service Graph Connector for Nokia Altiplano by selecting the ![](../../../reuse/icons/product-icons/globe-outline-24.svg) icon, searching for Nokia Altiplano, and selecting it.

![multi-instance.](../images/telecom-multi-instance.png)

### Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Nokia Altiplano** &gt; **Setup**.

2.  On the Getting started page, select **Get Started**.

    Repeat all the steps under the Configured Connectivity section. It creates configuration entries for the new instance of Nokia Altiplano.

    ![configure connectivity.](../images/telecom-connectivity.png)

3.  Select **Create Connection Alias**.

4.  Configure Create Connection Alias, Create Credentials, and Create HTTP Connection.

    ![configure connectivity.](../images/telecom-create-connection-alias.png)

    1.  Configure aliases for the connections and credentials:

        1.  Select **Configure**.

        2.  In the **Name** filed, specify the allies name.

        3.  Leave the rest of the fields as default, select **Submit**, and then **Mark as Complete**.
        ![connection and credential alias.](../images/telecom-connection-credential-alias.png)

        This enables using the connection by name rather than directly, enabling the collector to extract all active aliases from the CMDB and start performing data collection on the HTTP connection bound to it.

    2.  Create the relevant credentials to access the Nokia Altiplano Controller:

        1.  Select **Configure**.

        2.  In the **Name** field, specify your Nokia Altiplano instance user name.
        3.  In the **Password** field, specify your Nokia Altiplano instance password.

            **Note:** Other authentication fields may be required depending on the authentication methods used in your Nokia Altiplano instance.

        4.  Leave the rest of the fields as default, select **Submit** and then **Mark as Complete**.

    3.  Create HTTP Connection:

        1.  Select **Configure**.

        2.  In the **Name** filed, specify the HTTP connection name.

        3.  In the **Credentials** field, select the ![](../../../reuse/icons/product-icons/magnifying-glass-fill-24.svg) icon and select the credential defined in section 5.b

        4.  In the **Connection alias** field, select the ![](../../../reuse/icons/product-icons/magnifying-glass-fill-24.svg) icon and select the Connection allies.

        5.  In the **Connection URL** field, specify the Nokia Altiplano URL.

        6.  Check the **Use MID Server** check box and select the specific MID Server or MID Server Cluster to run discovery from.

        7.  Leave the rest of the fields as default, select **Submit** and then **Mark as Complete**.

        ![create http connection.](../images/telecom-create-http-connection.png)

5.  Test the connection by using the **Test Load 20 Records** related link.


