---
title: Create a WSDL for the SAP service definition
description: Generate a Web Services Description Language \(WSDL\) URL for the SAP service definition to use when creating SAP connections on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/create-wsdl-sap-service.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 2
keywords: [SAP WSDL, service definition, SOA Manager, SAP integration]
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create a WSDL for the SAP service definition

Generate a Web Services Description Language \(WSDL\) URL for the SAP service definition to use when creating SAP connections on your ServiceNow instance.

## Before you begin

The SAP transport files for your ServiceNow instance version must be available from the SAP ABAP Program for the Software Asset Management application. You must import the central transport request \(TR\) into the central system. If your satellite system is SAP S/4HANA, you must also import the corresponding satellite TR into the satellite system.

Role required: SAP Basis administrator

## About this task

After importing the transport files into your SAP system, configure the service binding in the SOA Manager and generate the WSDL URL. You must save the WSDL URL for use when creating SAP connections in your ServiceNow instance.

## Procedure

1.  In your SAP system, open the **SE80** \(Object Navigator\) transaction code.

2.  Verify that the ServiceNow service definition is active by navigating to **/NOW/SAMP** &gt; **Enterprise Services** &gt; **Service Definitions** &gt; **/NOW/SAMP** in the **Object Name** menu on the Object Navigator page.

    \[Omitted image "wsdl-service-definition.png"\] Alt text: Service Definition on the Object Navigator page

3.  After verification, navigate to the **SOAMANAGER** transaction code.

4.  On the Service Administration tab of the SOA Management page, select **Web service configuration**.

5.  On the Web Service Configuration page, in the **Search Criteria** section of the Object Search tab, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Object Type|`All`|
    |Object Name|`/NOW/SAMP`|

6.  Select **Search**.

7.  Select the search result **/NOW/SAMP**.

8.  On the **Configurations** tab of the service definition details, select **Create Service**.

9.  In step 1, on the Configuration of New Binding for Service Definition '/NOW/SAMP' page, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Service Name|`NOW_SAMP`|
    |Service Description Text|A brief description of the service.|
    |New Binding Name|`NOW_SAMP`|

    \[Omitted image "wsdl-binding-info.png"\] Alt text: Configuration of New Binding for Service Definition page showing

10. Select **Next**.

11. In step 2, set the **Transport Channel Authentication** method to **User ID/Password** in the Authentication Settings section.

12. Select **Finish** to complete the service configuration.

    The configuration is complete and you automatically return to the **Configurations** tab of the /NOW/SAMP service definition details.

13. Verify that the **NOW\_SAMP** service appears in the list of available services and bindings.

    \[Omitted image "wsdl-services.png"\] Alt text: Details of Service Definition screen showing available services and bindings

14. In the **NOW\_SAMP** list entry, select the **Open service WSDL generation** icon to generate a WSDL URL for the service.

15. Copy the URL from the **WSDL URL for Service** field and save it in a secure location for later use.

    You must activate all Internet Communication Framework \(ICF\) services in SICF before creating the SAP connection. To do this, run the SICF \(Maintain Services\) transaction on the front-end SAP server and select **Service/Host** &gt; **Activate** to activate the services.


## What to do next

Create SAP users, roles, and authorizations that can be used with the Software Asset Management integration. For details, see [Create SAP users, roles, and authorizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-sap-users-roles-auth.md).

**Parent Topic:**[Set up SAP integration to establish a connection with SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/setup-sap-integration.md)

