---
title: Deploy the ABAP program for SAP
description: To begin establishing a connection between your SAP system and your ServiceNow instance, deploy the Advanced Business Application Programming \(ABAP\) program. Deploying the ABAP program allows data to be shared between SAP and your ServiceNow instance.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Deploy the ABAP program for SAP

To begin establishing a connection between your SAP system and your ServiceNow instance, deploy the Advanced Business Application Programming \(ABAP\) program. Deploying the ABAP program allows data to be shared between SAP and your ServiceNow instance.

## Before you begin

To access the ABAP program, download the SAP ABAP for Software Asset Management application from the [ServiceNow Store](https://store.servicenow.com/). Make sure you download the application version that is compatible with the Yokohama release.

Role required: sam\_admin

## About this task

To deploy the ABAP program, import the transport files that are provided through the SAP ABAP for Software Asset Management application and then configure a service provider with the service-oriented architecture \(SOA\) Manager.

**Note:** If you upgrade your ServiceNow instance, you must download and deploy the version of the ABAP program that is compatible with the new release. You must then reconfigure a service provider with the SOA Manager.

For SAP setup information, see [KB0813999](https://support.servicenow.com/kb_view.do?sysparm_article=KB0813999).

For more information on SAP and its related tools, refer to the [SAP Help Portal](https://help.sap.com/viewer/index).

## Procedure

1.  In your SAP system, import the transport files using the SAP Transport Management System \(STMS\).

    1.  Copy and extract the `COFILE` and `DATA` files to your directory.

    2.  Start STMS and select **Import Overview**.

    3.  Double-click the target system, select **Extras** &gt; **Other Requests** &gt; **Add**, and then enter the transport request number.

    4.  Highlight the request and select **Request** &gt; **Import**.

    5.  From the Import Transport Request window, enter the client number in the **Target Client** field.

    6.  Select the Options tab, and then select the **Ignore Invalid Component Version** check box.

    7.  Select **OK**.

2.  In your SAP system, configure a service provider with the SOA Manager.

    1.  Start the SOA Manager and select **Service Administration** &gt; **Web Service Configuration**.

    2.  Select **Service Definition** from the **Search By** field.

    3.  Enter the service definition location in the **Search Pattern** field.

    4.  Select **Go**.

    5.  From the Search Results pane, select the service definition row, and then select **Apply Selection**.

    6.  From the Configurations tab, select **Create**.

    7.  Complete the following fields.

        |Field|Description|
        |-----|-----------|
        |Service Name|Name of the service.|
        |Description|Description of the service.|
        |New Binding Name|Name of the binding.|

    8.  Select **Apply Settings**.

    9.  Select **Provider Security** &gt; **Message Authentication**, and then select the **User ID/Password** check box.

    10. Select **Save**.

    11. Select **Overview** &gt; **Open Design time WSDL document**.

        A browser window opens and a new WSDL is generated.

    12. Select **Open Service WSDL Generation**.

    13. Copy the link from the **WSDL URL for Binding** field.

3.  Verify the RFC connection.


## What to do next

Return to your ServiceNow instance to establish your SAP connection.

**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Establish an SAP connection](add-sap-connection.md)

[Create entitlements for SAP](create-entitlement-sap.md)

[Create software models for SAP](add-software-model-sap.md)

[Create a custom SAP named user type](create-named-user.md)

[Map a role to a named user type](create-named-user-type-role-mapping.md)

[Create custom SAP price lists](create-sap-pricelist.md)

[Import custom SAP named user types](import-custom-sap-named-user-type.md)

[Import custom SAP price lists](import-custom-sap-price-list.md)

[SAP USMM-based optimization](../concept/usmm-optimization.md)

[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

