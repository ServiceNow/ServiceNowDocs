---
title: Configure a catalog in Service Portal
description: Associate a portal with multiple catalogs. By default, Service Portal is associated with Service Catalog.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure a catalog in Service Portal

Associate a portal with multiple catalogs. By default, Service Portal is associated with Service Catalog.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Click the **Service Portal** record.

3.  To associate a portal with a catalog, perform the following steps.

    1.  In the **Catalogs** related list, click **Edit**.

    2.  Select one or more catalogs to add to the portal.

        The categories and catalog items associated with the selected catalogs are displayed in Service Portal.

        **Note:**

        -   If no catalogs are selected, all active catalogs accessible to the requester are available in Service Portal.
        -   Irrespective of the catalogs associated with the portal, items are searched for only in the catalogs configured in the search source in AI Search. For information on configuring AI-based catalog search experience, see [Configure AI-based catalog search experience](https://www.servicenow.com/docs/access?context=config-ai-search-cat&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
4.  To edit the label for a catalog, perform the following steps.

    1.  For the **Main menu** field, click **Open Record**.

    2.  From the **Menu Items** section, Click the **Catalog** record.

    3.  In the **Label** field, specify the label for the catalog.

        The catalog label is displayed in the main menu of Service Portal.

5.  Click **Update**.


-   **[Access Management Automation](../concept/access-management.md)**  
Automate access management request fulfillment using the Service Catalog or Service Portal. The catalog items and flows support requests in Okta, Microsoft Entra ID \(formerly Microsoft Azure AD\), and Microsoft Active Directory.
-   **[Cloud Deployment Automation](../../../administer/integrationhub-store-spokes/concept/cloud-dep-auto.md)**  
Automates the deployment and provisioning of the AWS CloudFormation services using Service Catalog or Service Portal.

**Parent Topic:**[Create a portal](create-a-portal.md)

**Related topics**  


[Service Catalog in Service Portal](https://www.servicenow.com/docs/access?context=catalog-on-portal&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

