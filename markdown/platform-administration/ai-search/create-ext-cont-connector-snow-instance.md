---
title: Create a ServiceNow instance external content connector
description: Create an external content connector to retrieve searchable content and security principals from a ServiceNow AI Platform instance.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow instance external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a ServiceNow instance external content connector

Create an external content connector to retrieve searchable content and security principals from a ServiceNow AI Platform instance.

## Before you begin

A user with the admin role must have already configured your ServiceNow AI Platform source instance to allow access by the ServiceNow instance external content connector. For details on configuring these settings on your source instance, see [Configure your ServiceNow AI Platform instance for external content indexing](configure-sn-aip-instance-external-content-indexing.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

Create a ServiceNow® instance external content connector to retrieve content and metadata from a remote source instance and make it searchable on the destination instance where the connector runs.

You can only create one ServiceNow® instance external content connector on a given destination instance.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **ServiceNow Instance** tile, then select **Next**.

5.  On the Connection settings page, fill in the connection settings.

<table id="table_uvz_jrv_sdc"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this ServiceNow instance external content connector. You may find it useful to name the connector to match your source instance's hostname. As an example, if your source instance is `https://example-prod.service-now.com/`, you might enter `Example-Prod` as the connector name.

</td></tr><tr><td>

Instance URL

</td><td>

URL for the ServiceNow AI Platform source instance that you want to crawl searchable content from. As an example, you might enter `https://example-prod.service-now.com/`.

</td></tr><tr><td>

User Name

</td><td>

User ID for the service user defined in your ServiceNow AI Platform source instance. If you don't know the service user's ID, ask the admin who configured the ServiceNow AI Platform source instance for external content indexing for it.

</td></tr><tr><td>

Password

</td><td>

Password for the service user defined in your ServiceNow AI Platform source instance. If you don't know the service user's password, ask the admin who configured the ServiceNow AI Platform source instance for external content indexing for it.

</td></tr></tbody>
</table>6.  Save and validate your connection settings by selecting **Validate Connection**.

    **Note:** If validation of your connection settings fails, the system shows an error message. Double-check your connection settings to ensure they're correct. If permissions required by the connector are missing or incorrectly configured in the source system, a warning message appears showing the permissions that need to be corrected. Provide the information from this message to your source system administrator.

7.  Once your connection settings are validated, select **Next**.

8.  On the Crawl settings page, modify any default crawl settings that you want to override for this connector, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the crawl settings for this connector from the External Content Admin Home page. For details on this procedure and the available crawl settings, see [Configure crawl settings for a ServiceNow instance external content connector](configure-crawl-settings-snow-instance-external-content-connector.md).

9.  On the User permission settings page, modify any default user permission settings that you want to override for this connector.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the user permission settings for this connector from the External Content Admin Home page. For details on this procedure and user permission settings, see [Configure user permission settings for an external content connector](configure-user-mapping-settings-external-content-connector.md).

10. On the Create crawl page, create a content crawl for this connector by selecting a crawl scope \(if supported\) and any desired options, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can create and run crawls for this connector from the External Content Admin Home page. For details on creating content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

11. On the Connect search profile page, use the **Connect to search profile** field and **Add** button to add any search profiles that you want to connect this external content connector's default search source to, then select **Save**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can connect search sources for this connector to search profiles from the External Content Admin Home page. For details on connecting an external content connector to search profiles, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).


## Result

Your new external content connector appears in the Connectors list on the External Content Admin Home page.

## What to do next

To retrieve searchable content and security principals with your new connector, you need to configure and run content and user mapping crawls for it. You can modify your new connector's crawl settings and create crawls for it from the External Content Admin Home page even if you skipped these steps during connector creation.

-   To learn how to configure your new connector's crawl settings, see [Configure crawl settings for a ServiceNow instance external content connector](configure-crawl-settings-snow-instance-external-content-connector.md).
-   For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md) and [Create a user permission crawl for an external content connector](create-user-mapping-crawl-external-content-connector.md).

To make content crawled by your new connector searchable in portals and search applications, you need to link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](../concept/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).

**Parent Topic:**[ServiceNow instance external content connector](../concept/servicenow-instance-external-content-connector.md)

