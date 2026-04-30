---
title: Create a content crawl for an external content connector
description: Retrieve searchable content and metadata from your source system with a content crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-05"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Crawl, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a content crawl for an external content connector

Retrieve searchable content and metadata from your source system with a content crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.

## Before you begin

To run crawls for external content connectors, your instance must have inbound mTLS support enabled. For details on verifying that this feature is enabled on your instance, see [Verify whether inbound mTLS support is enabled for your instance](verify-adcv2-inbound-mtls-enabled.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

Search administrators can retrieve searchable content and metadata from an external content connector's source system by creating a content crawl for the connector. Search administrators can specify the crawl's scope: a full content crawl retrieves searchable content and metadata from all available locations \(called start points\) in your source system, while a partial content crawl only retrieves content and metadata from a single specified start point and its descendants. A content crawl may take hours or days to complete, depending on the amount of content available in your source system and the scope of the crawl.

**Note:** Both full and partial content crawls honor the crawl settings defined for your external content connector, including any inclusion/exclusion content filters. Running a full content crawl does not bypass these settings.

Some external content connectors include an **Update user permissions** content crawl option. When you select this option, running the crawl launches both a content crawl and a user permission crawl for your source system. For more details on user permission crawls, see [Create a user permission crawl for an external content connector](create-user-mapping-crawl-external-content-connector.md).

You can run a content crawl as a one-time task or set it to recur on a scheduled basis.

**Note:** Beginning with External Content Connectors 6.0, the External Content Connectors application allows a maximum of five connector crawls to run simultaneously on your ServiceNow AI Platform® instance. Both content crawls and user permission crawls count against this limit. You can schedule and run external content connector crawls throughout the day to avoid overlap, or create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the connector that you want to create a content crawl for.

3.  In the connector editor's Create crawls tab, select **Crawl content**.

    The Crawl content dialog box appears.

4.  Select the tile for the scope you want for your content crawl.

    -   To retrieve searchable content and metadata from all available start points in your source system, select **Full content crawl**.
    -   To only retrieve searchable content and metadata from a single start point, select **Partial content crawl** and enter or select the start point for the crawl. The partial crawl will only retrieve content from this start point and its descendant locations.

        **Note:** When configuring a partial content crawl, you can select **Refresh start points** to populate the list of available start points. Refreshing this list requires retrieval of data from the source system and may take a minute or two.

    **Note:** If the **Partial content crawl** tile isn't shown, the external content connector only supports full content crawls.

5.  To configure your content crawl to launch a user permission crawl \(retrieving security principals from your source system\) when it runs, select the **Update user mappings** option.

    **Note:** If the **Update user permissions** option isn't shown, the external content connector doesn't support launching user permission crawls from content crawls.

6.  To make your content crawl run on a recurrent schedule, select the **Make recurring** option, then specify the schedule options.

    **Note:** If the **Make recurring** option isn't shown, the external content connector automatically schedules its own content crawls. In this case, you can only run one-time content crawls.

    1.  Enter a name for your scheduled crawl.

    2.  Select **Daily** or **Weekly** as the frequency for your scheduled crawl.

    3.  If you selected **Weekly** as the crawl frequency, select the options for the days of the week that you want your scheduled crawl to run on.

    4.  Specify when you want the system to run your scheduled crawl by entering its start time and selecting a time zone.

        The start time should be in **hh:mm a** format, where the format parameters have the following values:

        -   **hh**: a one- or two-digit hour between 0 and 12 inclusive, such as `5` or `11`
        -   **mm**: a two-digit minute between 00 and 59 inclusive, such as `15` or `37`
        -   **a**: any of `A`, `a`, `AM`, or `am` for AM \(morning\) or any of `P`, `p`, `PM`, or `pm` for PM \(afternoon\)
7.  Create your new content crawl by selecting the appropriate option.

    -   If you skipped step [6](create-content-crawl-external-content-connector.md#schedule-crawl), select **Create one-time crawl**.
    -   If you selected the **Make recurring** option in step [6](create-content-crawl-external-content-connector.md#schedule-crawl), select **Create crawl schedule**.

## Result

If you skipped step [6](create-content-crawl-external-content-connector.md#schedule-crawl), your new content crawl is added to the system's crawl queue. The system runs your crawl when it has resources available to do so.

If you selected the **Make recurring** option in step [6](create-content-crawl-external-content-connector.md#schedule-crawl), your new crawl appears in the Crawl schedules list in the external content connector editor's Create crawls tab.

## What to do next

You can monitor your content crawl's status or review its results using the crawl history and analytics. For details on these metrics, see [Review crawl history for an external content connector](review-crawl-ext-cont-connector.md).

If you need to cancel your running content crawl, see [Cancel a running external content connector crawl](cancel-ext-cont-connector-crawl.md).

**Parent Topic:**[Crawling content with External Content Connectors](../concept/using-ext-cont-connectors.md)

