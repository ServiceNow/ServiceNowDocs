---
title: Create an Amazon S3 external content connector
description: Create an external content connector to retrieve searchable content from your Amazon S3 source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/create-ext-cont-connector-amazon-s3.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 7
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Amazon S3 external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an Amazon S3 external content connector

Create an external content connector to retrieve searchable content from your Amazon S3 source system.

## Before you begin

A source system administrator must have already configured your Amazon S3 source system to allow access by the Amazon S3 external content connector. For the required source system configuration steps, see [Configure Amazon S3 for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-amazon-s3-external-content-indexing.md).

Role required: sn\_ext\_conn.xcc\_admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You must be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **Amazon S3** tile, then select **Next**.

5.  On the Connection settings page, fill in the connection settings.

<table id="table_uvz_jrv_sdc"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this Amazon S3 external content connector.

</td></tr><tr><td>

Access Key Id

</td><td>

Access key ID for the Amazon Web Services \(AWS\) IAM user account used by the Amazon S3 external content connector. If you don't have this access key ID, ask your AWS administrator for it.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret access key for the Amazon Web Services \(AWS\) IAM user account used by the Amazon S3 external content connector. If you don't have this secret access key, ask your AWS administrator for it.

</td></tr><tr><td>

I agree to the following legal disclaimer

</td><td>

Option acknowledging that the Amazon S3 external content connector makes all crawled content accessible by all search users. Amazon S3 content access permissions don't rely on users' email addresses, as retrieved in user permission crawls. As a result, user permission crawls aren't supported for the Amazon S3 external content connector.

</td></tr></tbody>
</table>6.  Expand the **Advanced connection settings** section and fill in the fields.

<table id="table_u4x_znw_gkc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Endpoint resolution

</td><td>

Selection mode for the AWS endpoint to use for connection and authentication.Supported values:

-   **Automatic**: The connector uses the AWS SDK and your **AWS region** and **Use FIPS compliant endpoints** settings to automatically select the AWS endpoint to use.
-   **Manual**: The connector uses the AWS endpoint and region that you specify in the **Endpoint** and **AWS region** fields.


</td></tr><tr><td>

Use FIPS compliant endpoints

</td><td>

Option to force connection and authentication operations to use an AWS endpoint host that conforms to the Federal Information Processing Standards.This option appears only when you set **Endpoint resolution** to **Automatic**. It's only accessible when the region specified in the **AWS region** field supports FIPS endpoints.

</td></tr><tr><td>

Endpoint

</td><td>

URL for the AWS endpoint host you want the connector to use for connection and authentication. As an example, to make the connector use the `s3.us-east-1.amazonaws.com` endpoint with the HTTPS protocol, you might enter `https://s3.us-east-1.amazonaws.com`.This field appears only when you set **Endpoint resolution** to **Manual**.

For the full list of supported endpoints, see the [Amazon Simple Storage Service endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/s3.html) Amazon documentation resource.

**Note:** The Amazon resource lists endpoint hostnames. This field's value must be a valid URL, with the HTTP or HTTPS protocol prefix included.

</td></tr><tr><td>

AWS region

</td><td>

AWS region containing your Amazon S3 buckets. As an example, you might specify `us-west-1`.When **Endpoint resolution** is set to **Automatic**, the connector uses this region and the **Use FIPS compliant endpoints** option to determine the correct AWS endpoint to use for connection and authentication.

To view the list of AWS regions, see the [Amazon Simple Storage Service endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/s3.html) Amazon documentation resource.

**Note:** For regulatory market compliance, specify a regulated market AWS region, such as `us-gov-east-1` or `us-gov-west-1`.

</td></tr><tr><td>

Buckets

</td><td>

List of Amazon S3 buckets containing your content. Enter a bucket name and press **Add** to add it to the list.You must populate this field when using an AWS endpoint that doesn't support automatic bucket discovery, such as a FIPS endpoint or an Amazon S3 Outposts endpoint. For other endpoints, you can leave this field empty to enable auto-discovery of buckets.

When this list is populated, the connector only retrieves searchable content and metadata from the specified Amazon S3 buckets.

</td></tr></tbody>
</table>7.  Save and validate your connection settings by selecting **Validate Connection**.

    **Note:** If validation of your connection settings fails, the system shows an error message. Verify your connection settings to ensure they're correct. If permissions required by the connector are missing or incorrectly configured in the source system, a warning message appears showing the permissions that must be corrected. Provide the information from this message to your source system administrator.

8.  On the Crawl settings page, modify any default crawl settings that you want to override for this connector, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the crawl settings for this connector from the External Content Admin Home page. For details on this procedure and the available crawl settings, see [Configure crawl settings for an Atlassian Confluence Cloud external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-cc-ext-cont-connector.md).

9.  On the Create crawl page, create a content crawl for this connector by selecting a crawl scope \(if supported\) and any desired options, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can create and run crawls for this connector from the External Content Admin Home page. For details on creating content crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md).

10. On the Connect search profile page, use the **Connect to search profile** field and **Add** button to add any search profiles that you want to connect this external content connector's default search source to, then select **Save**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can connect search sources for this connector to search profiles from the External Content Admin Home page. For details on connecting an external content connector to search profiles, see [Connect an external content connector to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/connect-external-content-connector-search-profile.md).

    When you link a connector search source to a search profile in this step, the system automatically publishes the search profile to make the new link take effect.


## Result

Your new external content connector appears in the Connectors list on the External Content Admin Home page.

## What to do next

To retrieve searchable content with your new connector, you must configure and run content crawls for it. You can modify your new connector's crawl settings and create crawls for it from the External Content Admin Home page even if you skipped these steps during connector creation.

-   To learn how to configure your new connector's crawl settings, see [Configure crawl settings for an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-amazon-s3-external-content-connector.md).
-   For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md).

**Important:** All content the connector retrieves from your Amazon S3 buckets is treated as public content, searchable by everyone who has access to your configured AI Search experience.

To make content crawled by your new connector searchable in portals and search applications, you must link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/connect-external-content-connector-search-profile.md).

**Parent Topic:**[Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/amazon-s3-external-content-connector.md)

