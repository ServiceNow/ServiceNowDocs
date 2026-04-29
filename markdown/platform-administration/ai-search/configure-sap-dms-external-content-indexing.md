---
title: Configure SAP DMS for external content indexing
description: Create service instances and service keys in your SAP Business Technology Platform \(BTP\) global account to allow the SAP DMS external content connector to access your SAP DMS documents and repositories.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 13
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [SAP DMS external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure SAP DMS for external content indexing

Create service instances and service keys in your SAP Business Technology Platform \(BTP\) global account to allow the SAP DMS external content connector to access your SAP DMS documents and repositories.

## Before you begin

You must be a global account administrator on the SAP BTP. Your global account must be authorized to access the SAP Document Management Service.

A SAP global account administrator must have created a subaccount in your SAP BTP global account, with these entitlements:

-   Document Management Service, Application Option
-   Document Management Service, Integration Option
-   Document Management Service, Repository Option
-   Cloud Foundry Environment
-   Authorization and Trust Management Service

If you don't already have a subaccount with these entitlements in your SAP BTP global account, perform the [Create a subaccount in the SAP Business Technology Platform \(BTP\)](create-subaccount-sap-btp.md) preliminary task before performing this task.

Role required: none

## About this task

The SAP DMS external content connector retrieves documents from repositories in your SAP DMS source system using the Document Management Service, Integration Option REST API.

To allow the connector to access your SAP DMS source system via this API, you must configure service instances and service keys in the SAP DMS Business Technology Platform \(BTP\). Your connector admin can use settings copied from your new service keys to configure the SAP DMS external connector for proper connection to your source system.

## Procedure

1.  Create a service instance for the Document Management Service, Application Option in your subaccount.

    1.  Log in to the SAP Business Technology Platform \(BTP\) at [https://cockpit.btp.cloud.sap/](https://cockpit.btp.cloud.sap/) using your global account credentials.

    2.  In the Subaccounts tab, select your subaccount.

    3.  Navigate to **Service Marketplace**.

    4.  Search for and select the **Document Management Service, Application Option** entry.

    5.  Select **Create**.

    6.  On the New Instance or Subscription form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Plan|Select **standard**, then select the disclaimer option.|
        |Runtime Environment|Select **Cloud Foundry**.|
        |Space|Enter the name of the Cloud Foundry space you created for your subaccount. If you followed the subaccount creation steps from [Create a subaccount in the SAP Business Technology Platform \(BTP\)](create-subaccount-sap-btp.md), this name is `DMS`.|
        |Instance Name|Enter a name of your choice. As an example, you might enter `DMS-AO`.|

    7.  Select **Create**.

        SAP BTP creates the Document Management Service, Application Option service instance in your subaccount.

2.  Create a service key for your new Document Management Service, Application Option service instance.

    1.  From your subaccount, navigate to **Instances and Subscriptions**.

    2.  In the Subscriptions tab, in the row for your new Document Management Service, Application Option service instance, select **…** &gt; **Create Service Key**.

    3.  On the New Service Key form, enter a name for your new service key.

        As an example, you might enter `DMS-AO`.

    4.  Select **Create**.

        SAP BTP creates the Document Management Service, Application Option service key in your subaccount.

3.  Create a service instance for the Document Management Service, Integration Option in your subaccount.

    1.  Log in to the SAP Business Technology Platform \(BTP\) at [https://cockpit.btp.cloud.sap/](https://cockpit.btp.cloud.sap/) using your global account credentials.

    2.  In the Subaccounts tab, select your subaccount.

    3.  Navigate to **Service Marketplace**.

    4.  Search for and select the **Document Management Service, Integration Option** entry.

    5.  Select **Create**.

    6.  On the New Instance or Subscription form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Plan|Select **standard**, then select the disclaimer option.|
        |Runtime Environment|Select **Cloud Foundry**.|
        |Space|Enter the name of the Cloud Foundry space you created for your subaccount. If you followed the subaccount creation steps from [Create a subaccount in the SAP Business Technology Platform \(BTP\)](create-subaccount-sap-btp.md), this name is `DMS`.|
        |Instance Name|Enter a name of your choice. As an example, you might enter `DMS-IO`.|

    7.  Select **Create**.

        SAP BTP creates the Document Management Service, Integration Option service instance in your subaccount.

4.  Create a service key for your new Document Management Service, Integration Option service instance and copy its client settings and API URL.

    1.  From your subaccount, navigate to **Instances and Subscriptions**.

    2.  In the Subscriptions tab, in the row for your new Document Management Service, Integration Option service instance, select **…** &gt; **Create Service Key**.

    3.  On the New Service Key form, enter a name for your new service key.

        As an example, you might enter `DMS-IO`.

    4.  Select **Create**.

        SAP BTP creates the Document Management Service, Integration Option service key in your subaccount.

    5.  In the Service Keys section, view your new service key by selecting **…** &gt; **View** in its entry.

    6.  On the Credentials form, copy the **clientid**, **clientsecret**, and **url** values from the **uaa** section and store them in a secure location.

        **Important:** Your external content connector admin needs these client setting values when configuring the SAP DMS external content connector.

    7.  On the Credentials form, copy the **url** field value from the endpoints section's ecmservice entry and store it in a secure location.

        **Important:** Your external content connector admin needs this endpoint URL when configuring the SAP DMS external content connector.

    8.  On the Credentials form, copy the **apiurl** field value and store it in a secure location.

        **Important:** Your external content connector admin needs this role collections endpoint URL when configuring the SAP DMS external content connector.

    9.  On the Credentials form, copy the portion of the **xsappname** field value that appears after the pipe \| symbol and store it in a secure location.

        As an example, if the **xsappname** field value is `673dc63a-f785-4225-b974-de10815701fc!b23581|sdm-di-DocumentManagement-sdm_integration!b62497`, the portion of the value to copy is `sdm-di-DocumentManagement-sdm_integration!b62497`.

5.  Create a service instance for the Document Management Service, Repository Option in your subaccount.

    1.  Log in to the SAP Business Technology Platform \(BTP\) at [https://cockpit.btp.cloud.sap/](https://cockpit.btp.cloud.sap/) using your global account credentials.

    2.  In the Subaccounts tab, select your subaccount.

    3.  Navigate to **Service Marketplace**.

    4.  Search for and select the **Document Management Service, Repository Option** entry.

    5.  Select **Create**.

    6.  On the New Instance or Subscription form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Plan|Select **standard**, then select the disclaimer option.|
        |Runtime Environment|Select **Cloud Foundry**.|
        |Space|Enter the name of the Cloud Foundry space you created for your subaccount. If you followed the subaccount creation steps from [Create a subaccount in the SAP Business Technology Platform \(BTP\)](create-subaccount-sap-btp.md), this name is `DMS`.|
        |Instance Name|Enter a name of your choice. As an example, you might enter `DMS-RO`.|

    7.  Select **Create**.

        SAP BTP creates the Document Management Service, Repository Option service instance in your subaccount.

6.  Create a service key for your new Document Management Service, Repository Option service instance.

    1.  From your subaccount, navigate to **Instances and Subscriptions**.

    2.  In the Subscriptions tab, in the row for your new Document Management Service, Repository Option service instance, select **…** &gt; **Create Service Key**.

    3.  On the New Service Key form, enter a name for your new service key.

        As an example, you might enter `DMS-RO`.

    4.  Select **Create**.

        SAP BTP creates the Document Management Service, Repository Option service key in your subaccount.

7.  Create a service instance for the Authorization and Trust Management Service in your subaccount.

    1.  From your subaccount, navigate to **Services** &gt; **Service Marketplace**.

    2.  Search for and select the **Authorization and Trust Management Service** entry.

    3.  Select **Create**.

    4.  On the New Instance or Subscription form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Plan|Select **apiaccess**.|
        |Runtime Environment|Select **Cloud Foundry**.|
        |Space|Enter the name of the Cloud Foundry space you created for your subaccount. If you followed the subaccount creation steps from [Create a subaccount in the SAP Business Technology Platform \(BTP\)](create-subaccount-sap-btp.md), this name is `DMS`.|
        |Instance Name|Enter a name of your choice. As an example, you might enter `ATMS`.|

    5.  Select **Next**.

    6.  On the New Instance or Subscription form, paste the following JSON code into the Configure instance parameters text entry field, replacing `<instance-name>` with the name of your ServiceNow AI Platform instance.

        ```json
        {
          "xsappname": "dms-servicenow-client",
          "tenant-mode": "dedicated",
          "description": "XSUAA config for DMS API access via IAS",
          "oauth2-configuration": {
            "redirect-uris": [
              "https://<instance-name>.service-now.com/oauth_redirect.do"
            ],
            "grant-types": [
              "authorization_code",
              "client_credentials",
              "password",
              "refresh_token"
            ]
          },
          "scopes": [
            {
              "name": "$XSAPPNAME.DMSViewer",
              "description": "Read-only access to DMS repositories"
            },
            {
              "name": "$XSAPPNAME.DMSContributor",
              "description": "Create and modify documents in DMS"
            },
            {
              "name": "$XSAPPNAME.DMSAdministrator",
              "description": "Full administrative access to DMS"
            }
          ],
          "role-templates": [
            {
              "name": "DMSViewerRole",
              "description": "Role for viewing DMS documents",
              "scope-references": [
                "$XSAPPNAME.DMSViewer"
              ]
            },
            {
              "name": "DMSContributorRole",
              "description": "Role for contributing documents",
              "scope-references": [
                "$XSAPPNAME.DMSContributor"
              ]
            },
            {
              "name": "DMSAdministratorRole",
              "description": "Role for administering DMS",
              "scope-references": [
                "$XSAPPNAME.DMSAdministrator"
              ]
            }
          ],
          "authorities": [
            "$XSAPPNAME.DMSViewer",
            "$XSAPPNAME.DMSContributor",
            "$XSAPPNAME.DMSAdministrator"
          ]
        }
        ```

    7.  Select **Create**.

        SAP BTP creates the service instance for the Authorization and Trust Management Service in your subaccount.

8.  Create a service key for your new Authorization and Trust Management Service instance.

    1.  From your subaccount, navigate to **Instances and Subscriptions**.

    2.  In the Subscriptions tab, in the row for your new Authorization and Trust Management Service instance, select **…** &gt; **Create Service Key**.

    3.  On the New Service Key form, enter a name for your new service key.

        As an example, you might enter `ATMS`.

    4.  Select **Create**.

        SAP BTP creates the service key for the Authorization and Trust Management Service in your subaccount.

    5.  In the Service Keys section, view your new service key by selecting **…** &gt; **View** in its entry.

    6.  On the Credentials form, copy the **clientid**, **clientsecret**, and **url** values from the service key section and store them in a secure location.

        **Important:** Your external content connector admin needs these client setting values when configuring the SAP DMS external content connector.

9.  Create a new instance for the Authorization and Trust Management Service with the application plan in your SAP BTP subaccount.

    1.  From your subaccount, navigate to **Services** &gt; **Instances and Subscriptions**.

    2.  Select **Create**.

    3.  On the New Instance or Subscription form's Basic Info page, fill in the fields.

<table id="table_lwf_h3k_hhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service

</td><td>

Select **Authorization and Trust Management Service**.

</td></tr><tr><td>

Plan

</td><td>

Select **application**.

</td></tr><tr><td>

Runtime Environment

</td><td>

Select **Cloud Foundry**.

</td></tr><tr><td>

Space

</td><td>

Select **DMS**.**Note:** This is the name of the Cloud Foundry space you created for your SAP BTP subaccount. For details on this procedure, see [Create a subaccount in the SAP Business Technology Platform \(BTP\)](create-subaccount-sap-btp.md).

</td></tr><tr><td>

Instance Name

</td><td>

Enter a unique name for this service instance.

</td></tr></tbody>
</table>    4.  Select **Next**.

    5.  On the New Instance or Subscription form's Parameters page, paste the following JSON code into the Configure instance parameters text entry field, replacing `<service-name>` with the name you entered for the new Authorization and Trust Management Service instance with the application plan in step [9.c](configure-sap-dms-external-content-indexing.md#atms-app-plan-instance-step), `<instance-name>` with the name of your ServiceNow AI Platform instance, and `<xsappname>` with the **xsappname** substring that you copied in step [4.i](configure-sap-dms-external-content-indexing.md#copy-xsappname-step).

        ```json
        {
          "xsappname": "<service-name>",
          "tenant-mode": "dedicated",
          "description": "XSUAA config for DMS API access via IAS",
          "oauth2-configuration": {
            "redirect-uris": [
              "https://<instance-name>.service-now.com/oauth_redirect.do"
            ],
            "grant-types": [
              "authorization_code",
              "client_credentials",
              "password",
              "refresh_token"
            ]
          },
          "scopes": [
            {
              "name": "$XSAPPNAME.DMSViewer",
              "description": "Read-only access to DMS repositories"
            },
            {
              "name": "$XSAPPNAME.DMSContributor",
              "description": "Create and modify documents in DMS"
            },
            {
              "name": "$XSAPPNAME.DMSAdministrator",
              "description": "Full administrative access to DMS"
            }
          ],
          "role-templates": [
            {
              "name": "DMSViewerRole",
              "description": "Role for viewing DMS documents",
              "scope-references": [
                "$XSAPPNAME.DMSViewer"
              ]
            },
            {
              "name": "DMSContributorRole",
              "description": "Role for contributing documents",
              "scope-references": [
                "$XSAPPNAME.DMSContributor"
              ]
            },
            {
              "name": "DMSAdministratorRole",
              "description": "Role for administering DMS",
              "scope-references": [
                "$XSAPPNAME.DMSAdministrator"
              ]
            }
          ],
          "authorities": [
            "$ACCEPT_GRANTED_AUTHORITIES",
            "<xsappname>.sdmadmin",
            "<xsappname>.sdmbusinessadmin"
          ],
          "foreign-scope-references": [
            "<xsappname>.sdmuser",
            "<xsappname>.sdmadmin",
            "<xsappname>.sdmbusinessadmin"
          ]
        }
        ```

    6.  Select **Create**.

        SAP BTP creates the service instance for the Authorization and Trust Management Service with the application plan in your subaccount.

10. Create a service key for your new Authorization and Trust Management Service instance with the application plan.

    1.  From your subaccount, navigate to **Instances and Subscriptions**.

    2.  In the Subscriptions tab, in the row for your new Authorization and Trust Management Service instance with the application plan, select **…** &gt; **Create Service Key**.

    3.  On the New Service Key form, enter a name for your new service key.

        As an example, you might enter `ATMS-app-plan`.

    4.  Select **Create**.

        SAP BTP creates the service key for the Authorization and Trust Management Service instance with the application plan in your subaccount.

    5.  In the Service Keys section, view your new service key by selecting **…** &gt; **View** in its entry.

    6.  On the Credentials form, copy the **clientid** and **clientsecret** values from the service key section and store them in a secure location.

        **Important:** Your external content connector admin needs these client setting values when configuring the SAP DMS external content connector.

11. Copy the base web URL for documents in your SAP DMS tenant.

    1.  Log in to your SAP DMS tenant using your global account credentials.

    2.  Navigate to a repository of your choice.

    3.  In the repository, navigate to a folder of your choice that contains one or more documents.

    4.  Select **…** in any document entry, then select **Show properties** from the context menu.

    5.  Copy the **Web Link** for the document, then extract the base web URL and store it in a secure location.

        The base web URL is the portion of the **Web Link** URL that ends with `/open`. As an example, if the **Web Link** URL is `https://example.sap.com/cp.portal/site#user-display?sap-ui-app-id-hint=com.sap.ecm.sdm.user&/documents/v1/open/rep=ABCDE&obj=12345&vs=1`, the base web URL is `https://example.sap.com/cp.portal/site#user-display?sap-ui-app-id-hint=com.sap.ecm.sdm.user&/documents/v1/open`.

        **Important:** Your external content connector admin needs this base web URL when configuring the SAP DMS external content connector.


## What to do next

Provide the following items to your connector admin:

-   The client ID, client secret, and access token URL that you copied from the service key for the Document Management Service, Integration Option service instance in step [4.f](configure-sap-dms-external-content-indexing.md#copy-dms-io-client-settings-step).
-   The ecmservice endpoint URL that you copied from the service key for the Document Management Service, Integration Option service instance in step [4.g](configure-sap-dms-external-content-indexing.md#copy-dms-io-endpoint-url-step).
-   The role collections endpoint URL that you copied from the service key for the Document Management Service, Integration Option service instance in step [4.h](configure-sap-dms-external-content-indexing.md#copy-role-collections-endpoint-url-step).
-   The client ID, client secret, and access token URL that you copied from the service key for the Authorization and Trust Management Service instance in step [8.f](configure-sap-dms-external-content-indexing.md#copy-atms-credentials-step).
-   The client ID and client secret that you copied from the service key for the Authorization and Trust Management Service instance with the application plan in step [10.f](configure-sap-dms-external-content-indexing.md#copy-token-exchange-settings-step).
-   The base web URL that you copied in step [11.e](configure-sap-dms-external-content-indexing.md#copy-base-web-url-step).

Your connector admin needs these items to configure a SAP DMS external content connector to retrieve documents and security principals from your SAP DMS source system.

For details on creating and configuring a SAP DMS external content connector, see [Create a SAP DMS external content connector](create-ext-cont-connector-sap-dms.md).

**Parent Topic:**[SAP DMS external content connector](../concept/sap-dms-external-content-connector.md)

