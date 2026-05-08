---
title: Create a connection to ILMT or BigFix Inventory
description: If you're using an HTTP connection or you've finished the initial configuration for HTTPS, establish a connection between your IBM server and the ServiceNow AI Platform.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [ILMT and BigFix Inventory integrations, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create a connection to ILMT or BigFix Inventory

If you're using an HTTP connection or you've finished the initial configuration for HTTPS, establish a connection between your IBM server and the ServiceNow AI Platform.

## Before you begin

Role required: sam\_admin

## About this task

**Note:** If you're using an HTTP or HTTPS connection without the MID Server, the firewall port must be opened for connectivity to your ServiceNow instance IP address.

## Procedure

1.  Navigate to **All** &gt; **Integration — ILMT / BigFix Inventory** &gt; **Setup**.

2.  On the **Connections** related tab of the Connection &amp; Credential Aliases form, select **New**.

    The HTTP\(s\) Connection form opens.

    ![HTTPs Connection form.](../image/ibm-ilmt-connection-form.png)

3.  On the form, fill in the fields.

<table id="table_x3l_x4d_c1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_qxj_bbq_zhb"><td>

Name

</td><td>

Unique name of the connection.

</td></tr><tr><td>

Credential

</td><td>

Credentials that are used to establish the connection. You can use either basic authentication credentials, such as a username and password, or API key credentials.**Note:** Select the same credentials that you use to access the ILMT server.

</td></tr><tr id="row_tmb_cbq_zhb"><td>

Connection alias

</td><td>

Connection alias with which the connection can be referred. This connection alias resolves your connection and credentials at runtime.

 This field is automatically set to the **sn\_samp\_ibm.IBMServers** alias.

</td></tr><tr id="row_ljy_cbq_zhb"><td>

Active

</td><td>

Option indicating that the connection is active.

</td></tr><tr id="row_t5g_dbq_zhb"><td>

Domain

</td><td>

Domain to which the connection belongs.

</td></tr></tbody>
</table>4.  Specify the URL for the connection.

    Depending on whether you are using an HTTP or HTTPS connection, use one of the following options to specify the connection URL:

    -   **HTTP connection**: Specify the HTTP connection URL using the **Connection URL** field.

        In the **Connection URL** field, enter a URL in the `http://<*host-ip-address\|dns-hostname*>:<*port*>` format.

        ![Connection URL field.](../image/ibm-ilmt-connection-url.png)

        **Note:** You cannot modify the **Connection URL** field if you select the **URL builder** check box.

    -   **HTTPS connection**: Specify the HTTPS connection URL using either the URL builder or an SSL certificate.

<table id="table_gcx_dpn_q5b"><thead><tr><th>

HTTPS Connection URL Option

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

URL builder

</td><td>

1.  To enable your ServiceNow instance to build a connection URL using the URL builder, select the **URL builder** check box.

The **Mutual authentication**, **Protocol**, **Host**, **Override default port**, and **Base path** fields appear on the form.

![Selecting the URL builder check box.](../image/ibm-ilmt-url-builder.png)

2.  In the **Protocol** field, specify the underlying protocol that is used by the connection.

This field is automatically set to **https**.

3.  In the **Host** field, enter the URL of the target host that is used by the connection.

You must enter a URL in the `https://<*host-ip-address\|dns-hostname*>:<*port*>` format.

4.  \(Optional\) In the **Override default port** field, enter the port number of the target port that is used by the connection.

You must enter the same port number that you used for your ILMT or BigFix Inventory setup.

5.  \(Optional\) In the **Base path** field, enter the base path for the connection.


</td></tr><tr><td>

SSL certificate

</td><td>

1.  Retrieve an SSL certificate from your IBM server.
2.  Depending on whether you are using an HTTPS connection with or without the MID Server, use one of the following options to apply the certificate to your ServiceNow instance:
    -   Without the MID Server:
        1.  In a new tab or window, upload the certificate to your ServiceNow instance.

Refer to [HTTPS without the MID Server](../concept/setting-up-ibm-ilmt.md#) for detailed instructions.

        2.  Return to the HTTP\(s\) Connection form.
        3.  Enable your ServiceNow instance to build a connection URL by selecting the **URL builder** check box.

The **Mutual authentication**, **Protocol**, **Host**, **Override default port**, and **Base path** fields appear on the form.

![Selecting the URL builder check box.](../image/ibm-ilmt-url-builder.png)

        4.  Enable mutual authentication for the connection by selecting the **Mutual authentication** check box.

The **Protocol** field is replaced by the **Protocol profile** field.

![Selecting the Mutual authentication check box.](../image/ibm-ilmt-url-builder-mutual-auth.png)

        5.  In the **Protocol profile** field, select the search icon \(![Search icon](../image/search-icon.png)\) to locate and select the HTTPS protocol profile that specifies the certificate used for mutual authentication.

You must select the same protocol profile that you created in [HTTPS without the MID Server](../concept/setting-up-ibm-ilmt.md#).

    -   With the MID Server:
        1.  In a new tab or window, upload the certificate to your ServiceNow instance.

Refer to [HTTPS with the MID Server](../concept/setting-up-ibm-ilmt.md#) for detailed instructions.

        2.  Return to the HTTP\(s\) Connection form and then select the **Use MID server** check box.

The **Advanced MID Server Configuration** tab appears.

![Selecting the Use MID server check box.](../image/ibm-ilmt-use-mid-server.png)

        3.  In the **MID Selection** field of the **Advanced MID Server Configuration** tab, specify how you want to select a MID Server for the connection.

Select one of the following options:

            -   **Auto-select MID Server**: Automatically selects a MID Server from the list of MID Servers that are configured for the connection. This option is selected by default.

If you select this option, the **Advanced MID Server Configuration** tab displays the **Capabilities** and **MID Application** fields. You can use these fields to filter the list of available MID Servers based on supported MID Server capabilities and applications.

                -   To filter this list based on MID Server capabilities, select the Unlock Capabilities icon \(![Unlock capabilities icon.](../image/unlock-icon.png)\) in the **Capabilities** field. After you unlock the field, select the Lookup using list icon \(![Lookup using list icon.](../image/search-icon.png)\) to search for and select the desired capabilities.
                -   To filter this list based on MID Server applications, select the Lookup using list icon \(![Lookup using list icon.](../image/search-icon.png)\) in the **MID Application** field to search for and select the desired applications.
See MID Server selection for more information on MID Server capabilities and applications.

            -   **Specific MID Server**: Enables you to select a specific MID Server for the connection.

If you select this option, the **Advanced MID Server Configuration** tab displays the **MID Server** field. Select the Lookup using list icon \(![Lookup using list icon.](../image/search-icon.png)\) in the **MID Server** field to search for and select the MID Server that you want to use for the connection.

**Important:** To select a specific MID Server for the connection, you must deselect the **Included in application ALL** check box for any applications that are configured to use the specified MID Server. For more information on this check box, refer to the Select applications to include in the definition of ALL for a MID Server section of Configure a default MID Server for each application.

            -   **Specific MID Cluster**: Enables you to select a specific MID Server cluster for the connection.

If you select this option, the **Advanced MID Server Configuration** tab displays the **MID Cluster** field. Select the Lookup using list icon \(![Lookup using list icon.](../image/search-icon.png)\) in the **MID Cluster** field to search for and select the MID Server cluster that you want to use for the connection.

</td></tr></tbody>
</table>5.  Set up the connection timeout.

    Use one of the following options to set up the connection timeout:

    -   **glide.http.outbound.max\_timeout.enabled system property**: The ServiceNow AI Platform **glide.http.outbound.max\_timeout.enabled** system property enables you to specify the number of seconds that RESTMessageV2 and SOAPMessageV2 APIs wait for a response from a synchronous call. You can configure this system property by opening a new tab or window and then navigating to **System Properties** &gt; **All Properties** &gt; **glide.http.outbound.max\_timeout.enabled**. If this system property is set to **true** or is not available on your ServiceNow instance, your instance uses a default timeout value of 30 seconds. If this system property is set to **false**, your ServiceNow instance uses a default timeout value 600 seconds. See Available system properties for more information on this system property.
    -   **Connection timeout field**: The **Connection timeout** field on the HTTP\(s\) Connection form enables you to specify the number of seconds that your ServiceNow instance waits to establish the given connection.

        **Important:** This option is applicable only in the San Diego and later releases. In the Rome and earlier releases, you must set up the connection timeout using only the **glide.http.outbound.max\_timeout.enabled** system property.

        Application of the **Connection timeout** field is dependent on your **glide.http.outbound.max\_timeout.enabled** system property configuration. If the system property is set to **false**, your ServiceNow instance honors the value that is specified in the **Connection timeout** field.

        **Note:** If the **Connection timeout** field is empty, your ServiceNow instance uses a default connection timeout value of 300 seconds.

        If the system property is set to **true** or is not available on your ServiceNow instance, your instance ignores the value that is specified in the **Connection timeout** field. Instead, your instance uses a default connection timeout value of 30 seconds.

6.  Configure additional attributes for the connection.

    Select the **Attributes** tab and then fill in the fields.

    ![Attributes tab on the HTTPs Connection form.](../image/ibm-ilmt-connection-form-attributes-tab.png)

<table id="table_dx2_vrm_q5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

source

</td><td>

Source of your IBM software installation data. The options are **ILMT** and **BigFix Inventory**.

</td></tr><tr><td>

computer\_system\_offset

</td><td>

Offset value that prevents your ServiceNow instance from re-importing computer records from ILMT or BigFix Inventory. Each time you run an import, the offset value updates automatically based on the computer records that are included in the import. Every subsequent import then retrieves only new computer records starting from the specified offset value.

 If you are establishing a new connection, verify that the offset value is set to **0**. If you want to re-import all computer records for an existing connection, reset the offset value to **0**.

</td></tr><tr><td>

virtual\_machine\_offset

</td><td>

Offset value that prevents your ServiceNow instance from re-importing virtual machine \(VM\) records from ILMT or BigFix Inventory. Each time you run an import, the offset value updates automatically based on the VM records that are included in the import. Every subsequent import then retrieves only new VM records starting from the specified offset value.

 If you are establishing a new connection, verify that the offset value is set to **0**. If you want to re-import all VM records for an existing connection, reset the offset value to **0**.

</td></tr></tbody>
</table>7.  Select **Submit**.

    The active connection information displays.

8.  If you are using version 1 of the ILMT and BigFix Inventory APIs, import ILMT or BigFix Inventory scheduled data manually.

    1.  Navigate to **Integration - ILMT / BigFix Inventory** &gt; **Scheduled Import** and then select **Execute Now**.

    2.  Verify that the import has completed successfully.

        -   To verify that both the import and transformation have completed successfully, navigate to **Integration - ILMT / BigFix Inventory** &gt; **Transform History**.

            **Note:** Every record in the Transform Histories table displays an **Inserts** value of `0`.

        -   To view all data that was imported into the License Consumption \[samp\_ilmt\_sw\_install\] table, navigate to **Integration - ILMT / BigFix Inventory** &gt; **Import Set Data** &gt; **License Consumption**.
        -   To view all data that was imported into the Computer \[cmdb\_ci\_computer\] table, navigate to **Integration - ILMT / BigFix Inventory** &gt; **Import Set Data** &gt; **Computers**.

**Parent Topic:**[IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](../concept/ibm-ilmt-bigfix-inventory-integration.md)

