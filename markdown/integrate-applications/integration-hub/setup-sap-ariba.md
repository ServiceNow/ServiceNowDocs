---
title: Set up the SAP Ariba spoke
description: Integrate the ServiceNow instance and SAP Ariba by using the SSH, Basic Auth, and API Key credentials to authenticate ServiceNow requests.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-11-03"
reading_time_minutes: 16
breadcrumb: [SAP Ariba Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the SAP Ariba spoke

Integrate the ServiceNow instance and SAP Ariba by using the SSH, Basic Auth, and API Key credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SAP Ariba spoke.
-   Role required: admin.

## About this task

For information about the connection and credential alias record that must be configured to use actions in an action category, see [Connection and credential alias requirements](../concept/sap-ariba-spoke.md#section_lr4_vjq_xmb).

## Procedure

1.  Configure the **SAP\_Ariba\_Import** connection and credential alias record.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the record, **SAP\_Ariba\_Import**.

    3.  Click the Create New Connection &amp; Credential related link.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Please Enter the Connection Information|
        |Connection Name|Name to identify the connection record. For example, `SAP Ariba Import Connection`.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://s1.ariba.com`|
        |Realm value|Realm of your SAP Ariba instance.|
        |Shared secret|Integration password provided for shared secret-based authentication. For more information, see [Shared secret-based authentication](https://help.sap.com/viewer/d066a90ef618101499ccd55dc3c29025/2003/en-US/d06bd10ff61810148780901700cabde1.html) in [SAP Help Portal](https://help.sap.com/viewer/index).|
        |Please Enter the Credential Information|
        |Credential Name|Name to identify the credential record. For example, `SAP Ariba Import Credential`.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Shared secret-based authentication](https://help.sap.com/viewer/d066a90ef618101499ccd55dc3c29025/2003/en-US/d06bd10ff61810148780901700cabde1.html) in [SAP Help Portal](https://help.sap.com/viewer/index).|

    5.  Click **Create**.

2.  Configure the **SAP\_Ariba\_Export** connection and credential alias record.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the record, **SAP\_Ariba\_Export**.

    3.  Click the Create New Connection &amp; Credential related link.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Please Enter the Connection Information|
        |Connection Name|Name to identify the connection record. For example, `SAP Ariba Export Connection`.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://s1.ariba.com`|
        |Realm value|Realm of your SAP Ariba instance.|
        |Please Enter the Credential Information|
        |Credential Name|Name to identify the credential record. For example, `SAP Ariba Export Credential`.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|

    5.  Click **Create**.

3.  Configure the **SAP\_Ariba\_Sourcing** connection and credential alias record.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the record, **SAP\_Ariba\_Sourcing**.

    3.  Click the Create New Connection &amp; Credential related link.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Please Enter the Connection Information|
        |Connection Name|Name to identify the connection record. For example, `SAP Ariba Sourcing Connection`.|
        |Connection URL|Integration Task **URL** created when you enabled SOAP service of the Import Sourcing Project task for the inbound endpoint in **Administration**. For information about Integration Task **URL** and **targetNamespace**, see [Enable an Integration Task](https://help.sap.com/viewer/f4204795aea64e909c53dc85a8030fdc/Cloud/en-US/2bd48cfaee3f4967b4d3fa3c87cf942b.html#loioeeaae4b5d8d84e5ba45bddfb8d8ccace) in [SAP Help Portal](https://help.sap.com/viewer/index).|
        |Target Namespace|Value of the **targetNamespace** parameter in WSDL file created in **Administration**. For information about Integration Task **URL** and **targetNamespace**, see [Enable an Integration Task](https://help.sap.com/viewer/f4204795aea64e909c53dc85a8030fdc/Cloud/en-US/2bd48cfaee3f4967b4d3fa3c87cf942b.html#loioeeaae4b5d8d84e5ba45bddfb8d8ccace) in [SAP Help Portal](https://help.sap.com/viewer/index).|
        |Please Enter the Credential Information|
        |Credential Name|Name to identify the credential record. For example, `SAP Ariba Sourcing Credential`.|
        |User Name|User name to log in to your SAP Ariba instance.|
        |Password|Login password provided under HTTP Authentication when you created an inbound endpoint in **Administration**. For information about creating an endpoint, see [Create New Integration End-Point](https://help.sap.com/docs/btp/sap-btp-neo-environment/configure-sap-ariba-solution?locale=en-US#create-new-integration-end-point) in [SAP Help Portal](https://help.sap.com/viewer/index).|

    5.  Click **Create**.

4.  Configure the **SAP\_Ariba\_Suppliers** connection and credential alias record.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the record, **SAP\_Ariba\_Suppliers**.

    3.  Click the Create New Connection &amp; Credential related link.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Please Enter the Connection Information|
        |Connection Name|Name to identify the connection record. For example, `SAP Ariba Suppliers Connection`.|
        |Connection URL|Integration Task **URL** created when you enabled SOAP service of the Import Sourcing Project task for the inbound endpoint in **Administration**. For information about Integration Task **URL** and **targetNamespace**, see [Enable an Integration Task](https://help.sap.com/viewer/f4204795aea64e909c53dc85a8030fdc/Cloud/en-US/2bd48cfaee3f4967b4d3fa3c87cf942b.html#loioeeaae4b5d8d84e5ba45bddfb8d8ccace) in [SAP Help Portal](https://help.sap.com/viewer/index).|
        |Target Namespace|Value of the **targetNamespace** parameter in WSDL file created in **Administration**. For information about Integration Task **URL** and **targetNamespace**, see [Enable an Integration Task](https://help.sap.com/viewer/f4204795aea64e909c53dc85a8030fdc/Cloud/en-US/2bd48cfaee3f4967b4d3fa3c87cf942b.html#loioeeaae4b5d8d84e5ba45bddfb8d8ccace) in [SAP Help Portal](https://help.sap.com/viewer/index).|
        |Please Enter the Credential Information|
        |Credential Name|Name to identify the credential record. For example, `SAP Ariba Sourcing Credential`.|
        |User Name|User name to log in to your SAP Ariba instance.|
        |Password|Login password provided under HTTP Authentication when you created an inbound endpoint in **Administration**. For information about creating an endpoint, see [Create New Integration End-Point](https://help.sap.com/docs/btp/sap-btp-neo-environment/configure-sap-ariba-solution?locale=en-US#create-new-integration-end-point) in [SAP Help Portal](https://help.sap.com/viewer/index).|

    5.  Click **Create**.

5.  Create an SSH credential record.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the record, **SAP Ariba SSH**.

    3.  In the **Credentials** tab, click **New**.

        The system displays the message `What type of Credentials would you like to create?`.

    4.  Select **SSH Credentials**.

    5.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the credential record. For example, `SAP Ariba SSH Credential`.|
        |User name|User name to log in to the Linux server on which the SFTP and SSH are set up.|
        |Password|Password to log in to the Linux server on which the SFTP and SSH are set up.|

        **Note:** The Linux server must be installed in the same network’s machine or virtual machine where your MID Server is installed.

    6.  Click **Submit**.

6.  Configure the **SAP Ariba Rest Procurement** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Integrations** tab.

    3.  Under **Connections**, toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Rest Procurement** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://s1.ariba.com`.|
        |API Version|API version of the SAP Ariba instance.|
        |Realm Value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.

7.  Configure the **SAP Ariba Rest Buyer** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Rest Buyer** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://s1.ariba.com`.|
        |API Version|API version of the SAP Ariba instance.|
        |Realm Value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Ariba Network ID|Unique identifier of the SAP Ariba network account.|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.

8.  Configure the **SAP Ariba Rest Sourcing** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Rest Sourcing** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://s1.ariba.com`.|
        |API Version|API version of the SAP Ariba instance.|
        |Realm Value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.

9.  Configure the **SAP Ariba Procurement Export** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Procurement Export** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://s1.ariba.com`.|
        |Realm Value|Realm of your SAP Ariba instance.|
        |Shared Secret|Integration password provided for shared secret-based authentication. For more information, see [Shared secret-based authentication](https://help.sap.com/viewer/d066a90ef618101499ccd55dc3c29025/2003/en-US/d06bd10ff61810148780901700cabde1.html) in [SAP Help Portal](https://help.sap.com/viewer/index).|

    8.  Click **Create Connection**.

10. Configure the **SAP Ariba SOAP Receipts** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba SOAP Receipts** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://s1.ariba.com`.|
        |Credential Information|
        |User name|User name to log in to your SAP Ariba instance.|
        |Password|Login password provided under HTTP Authentication when you created an inbound endpoint in Administration. For information about creating an endpoint, see [Create New Integration End-Point](https://help.sap.com/docs/btp/sap-btp-neo-environment/configure-sap-ariba-solution?locale=en-US#create-new-integration-end-point) in [SAP Help Portal](https://help.sap.com/viewer/index).|

    8.  Click **Create Connection**.

11. Configure the **SAP Ariba Procurement Import** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Procurement Import** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://s1.ariba.com`.|
        |Realm|Realm of your SAP Ariba instance.|
        |Credential Information|
        |Credential Name|Name to identify the credential record.|
        |User name|User name to log in to your SAP Ariba instance.|
        |Password|Login password provided under HTTP Authentication when you created an inbound endpoint in Administration. For information about creating an endpoint, see [Create New Integration End-Point](https://help.sap.com/docs/btp/sap-btp-neo-environment/configure-sap-ariba-solution?locale=en-US#create-new-integration-end-point) in [SAP Help Portal](https://help.sap.com/viewer/index).|

    8.  Click **Create Connection**.

12. Configure the **SAP Ariba Rest Suppliers** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Rest Suppliers** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://s1.ariba.com`.|
        |API Version|API version of the SAP Ariba instance.|
        |Realm value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.

13. Configure the **SAP Ariba Approvals Procurement** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Approvals Procurement** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://openapi.ariba.com/`.|
        |API Version|API version of the SAP Ariba instance.|
        |Realm value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.

14. Configure the **SAP Ariba Approvals Sourcing** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Approvals Sourcing** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://openapi.ariba.com/`.|
        |API Version|API version of the SAP Ariba instance.|
        |Realm value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.

15. Configure the **SAP Ariba Rest Event** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Rest Event** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://openapi.ariba.com/`.|
        |API Version|API version of the SAP Ariba instance.|
        |Realm value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.

16. Configure the **SAP Ariba Soap Requisition** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Soap Requisition** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Realm|Realm of your SAP Ariba instance.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://example.ariba.com/Buyer/soap/sample/RequisitionImportPull`.|
        |Credential Information|
        |User name|User name to log in to your SAP Ariba instance.|
        |Password|Login password provided under HTTP Authentication when you created an inbound endpoint in Administration. For information about creating an endpoint, see [Create New Integration End-Point](https://help.sap.com/docs/btp/sap-btp-neo-environment/configure-sap-ariba-solution?locale=en-US#create-new-integration-end-point) in [SAP Help Portal](https://help.sap.com/viewer/index).|

    8.  Click **Create and Get OAuth Token**.

17. Configure the **SAP Ariba Rest Invoices** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Rest Invoices** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Buyer Network ID|Unique identifier assigned to a buyer's organization within the Ariba Network.|
        |Shared Secret|Unique code or key used to authenticate the integration between the Ariba Network and ServiceNow instance.|
        |User Agent|Software or application used to access the Ariba Network.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://example.ariba.com`.|

    8.  Click **Create and Get OAuth Token**.

18. Configure the **SAP Ariba Async Reporting Job** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Async Reporting Job** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://openapi.ariba.com`.|
        |API version|API version of the SAP Ariba instance.|
        |Realm value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.

19. Configure the **SAP Ariba Rest Contracts** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Rest Contracts** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://openapi.ariba.com`.|
        |API version|API version of the SAP Ariba instance.|
        |Realm value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.

20. Configure the **SAP Ariba Rest Ship Notices** connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Connections** tab.

    3.  Toggle and enable the **Outbound** connections.

    4.  Search for **SAP Ariba Rest Ship Notices** connection.

    5.  Click **View Details**.

    6.  Click **Add Connection**.

    7.  On the form, fill in these values.

        |Field|Description|
        |-----|-----------|
        |Connection Information|
        |Connection Name|Name to identify the connection record.|
        |Connection URL|Base URL to connect to SAP Ariba instance. For example, `https://openapi.ariba.com`.|
        |API version|API version of the SAP Ariba instance.|
        |Realm value|Realm of your SAP Ariba instance.|
        |API Key|Integration password provided for shared secret-based authentication. For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).|
        |Credential Information|
        |OAuth Client ID|Client ID of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|
        |OAuth Client Secret|Client Secret of your SAP Ariba instance. For more information, see [Finding Your Application's Application Key and OAuth Client ID](https://help.sap.com/docs/ariba-apis/help-for-sap-ariba-developer-portal/finding-your-application-s-application-key-and-oauth-client-id) in [SAP Help Portal](https://help.sap.com/docs/).|

    8.  Click **Create and Get OAuth Token**.


## What to do next

Create buyer and supplier records in these spoke modules:

-   Supplier IDs Buyer
-   Supplier IDs Sourcing
-   Supplier Organizations Buyer
-   Supplier Organizations Sourcing

Actions in the sample flows require these records.

