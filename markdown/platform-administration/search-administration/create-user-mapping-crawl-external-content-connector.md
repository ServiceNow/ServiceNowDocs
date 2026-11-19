---
title: Create a user permissions crawl for an external content connector
description: Retrieve security principals from your source system with a user permissions crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-11-07"
reading_time_minutes: 5
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Crawl, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a user permissions crawl for an external content connector

Retrieve security principals from your source system with a user permissions crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.

## Before you begin

To run crawls for external content connectors, your instance must have inbound mTLS support enabled. For details on verifying that this feature is enabled on your instance, see [Verify inbound mTLS support activation for your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/verify-adcv2-inbound-mtls-enabled.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

Many external content connectors support preservation of access permissions for searchable content retrieved from their source systems. To use this feature, search administrators must retrieve security principals from the connector's source system by creating a user permissions crawl for the connector.

The user permissions crawl maps security principals retrieved from the source system to users in your ServiceNow AI Platform® instance. Each user that corresponds to a source system security principal inherits content access permissions specified for that security principal.

A user permissions crawl may take hours or days to complete, depending on the number of security principals defined in your source system.

You can run a user permissions crawl as a one-time task or set it to recur on a scheduled basis.

**Note:** Starting with External Content Connectors 6.0, the External Content Connectors application allows a maximum of five connector crawls to run simultaneously on your ServiceNow AI Platform® instance. Both content crawls and user permissions crawls count against this limit. You can schedule and run external content connector crawls throughout the day to avoid overlap, or create a Customer Service and Support case at [https://support.servicenow.com/now?draw=case](https://support.servicenow.com/now?draw=case) to request a limit increase.

For external content connectors that support user permissions crawls, you can also start a user permissions crawl by selecting the **Crawl user permissions** option when creating or scheduling a content crawl. For more details on this option and defining content crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-content-crawl-external-content-connector.md).

**Note:** The following external content connectors don't retrieve user or group access permissions. You can't run user permissions crawls for these connectors.

-   Adobe Experience Manager as a Cloud Service external content connector
-   Amazon S3 external content connector
-   Cornerstone external content connector
-   ServiceNow® product documentation external content connector
-   Slack external content connector
-   Trello external content connector
-   Webcrawler external content connector

The Atlassian Confluence Cloud external content connector only retrieves permissions for Confluence Cloud users who have made their email addresses visible to all users. To allow user mapping, each Confluence Cloud user must set their own email visibility to **Anyone** as explained in the [https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/](https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/) Atlassian support resource.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the connector that you want to create a user permissions crawl for.

3.  In the connector editor's **Create crawls** tab, select **Crawl user permissions**.

    The Crawl user permissions dialog box appears, with the **User permissions crawl** tile selected.

4.  To make your user permissions crawl run on a recurrent schedule, select the **Make recurring** option, then specify the schedule options.

    **Note:** If the **Make recurring** option isn't shown, the external content connector automatically schedules its own user permissions crawls. In this case, you can only run one-time user permissions crawls.

    1.  Enter a name for your scheduled crawl.

    2.  Select **Daily** or **Weekly** as the frequency for your scheduled crawl.

    3.  If you selected **Weekly** as the crawl frequency, select the options for the days of the week that you want your scheduled crawl to run on.

    4.  Specify when you want the system to run your scheduled crawl by entering its start time and selecting a time zone.

        The start time should be in **hh:mm a** format, where the format parameters have the following values:

        -   **hh**: a one- or two-digit hour between 0 and 12 inclusive, such as `5` or `11`
        -   **mm**: a two-digit minute between 00 and 59 inclusive, such as `15` or `37`
        -   **a**: any of `A`, `a`, `AM`, or `am` for AM \(morning\) or any of `P`, `p`, `PM`, or `pm` for PM \(afternoon\)
5.  Create your new user permissions crawl by selecting the appropriate option.

    -   If you skipped step [4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md), select **Crawl user permissions**.
    -   If you selected the **Make recurring** option in step [4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md), select **Create user crawl schedule**.

## Result

If you skipped step [4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md), your new user permissions crawl is added to the system's crawl queue. The system runs your crawl when it has resources available to do so.

If you selected the **Make recurring** option in step [4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md), your new crawl appears in the external content connector editor's **Manage crawls** tab.

## What to do next

You can monitor your user permissions crawl's status or review its results using the crawl history and analytics. For details on these metrics, see [Review crawl history for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/review-crawl-ext-cont-connector.md) and [Review user mappings for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/review-usr-maps-ext-cont-connector.md).

If you need to cancel your running user permissions crawl, see [Cancel a running external content connector crawl](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/cancel-ext-cont-connector-crawl.md).

**Parent Topic:**[Crawling content with External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/using-ext-cont-connectors.md)

