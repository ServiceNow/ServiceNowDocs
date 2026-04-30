---
title: Create a user permission crawl for an external content connector
description: Retrieve security principals from your source system with a user permission crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.
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

# Create a user permission crawl for an external content connector

Retrieve security principals from your source system with a user permission crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.

## Before you begin

To run crawls for external content connectors, your instance must have inbound mTLS support enabled. For details on verifying that this feature is enabled on your instance, see [Verify whether inbound mTLS support is enabled for your instance](verify-adcv2-inbound-mtls-enabled.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

Many external content connectors support preservation of access permissions for searchable content retrieved from their source systems. To use this feature, search administrators must retrieve security principals from the connector's source system by creating a user permission crawl for the connector.

The user permission crawl maps security principals retrieved from the source system to users in your ServiceNow AI Platform® instance. Each user that corresponds to a source system security principal inherits content access permissions specified for that security principal.

A user permission crawl may take hours or days to complete, depending on the number of security principals defined in your source system.

You can run a user permission crawl as a one-time task or set it to recur on a scheduled basis.

**Note:** Beginning with External Content Connectors 6.0, the External Content Connectors application allows a maximum of five connector crawls to run simultaneously on your ServiceNow AI Platform® instance. Both content crawls and user permission crawls count against this limit. You can schedule and run external content connector crawls throughout the day to avoid overlap, or create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase.

For external content connectors that support user permission crawls, you can also start a user permission crawl by selecting the **Update user permissions** option when creating or scheduling a content crawl. For more details on this option and defining content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Note:** The following external content connectors don't retrieve user or group access permissions. You can't run user permission crawls for these connectors.

-   Adobe Experience Manager as a Cloud Service external content connector
-   Amazon S3 external content connector
-   ServiceNow® product documentation external content connector
-   Slack external content connector
-   Trello external content connector
-   Webcrawler external content connector

The Atlassian Confluence Cloud external content connector only retrieves permissions for Confluence Cloud users who have made their email addresses visible to all users. To allow user permission, each Confluence Cloud user must set their own email visibility to **Anyone** as explained in the [https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/](https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/) Atlassian support resource.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the connector that you want to create a user permission crawl for.

3.  In the connector editor's Create crawls tab, select **Crawl user permissions**.

    The Crawl user permissions dialog box appears, with the **User permission crawl** tile selected.

4.  To make your user permission crawl run on a recurrent schedule, select the **Make recurring** option, then specify the schedule options.

    **Note:** If the **Make recurring** option isn't shown, the external content connector automatically schedules its own user permission crawls. In this case, you can only run one-time user permission crawls.

    1.  Enter a name for your scheduled crawl.

    2.  Select **Daily** or **Weekly** as the frequency for your scheduled crawl.

    3.  If you selected **Weekly** as the crawl frequency, select the options for the days of the week that you want your scheduled crawl to run on.

    4.  Specify when you want the system to run your scheduled crawl by entering its start time and selecting a time zone.

        The start time should be in **hh:mm a** format, where the format parameters have the following values:

        -   **hh**: a one- or two-digit hour between 0 and 12 inclusive, such as `5` or `11`
        -   **mm**: a two-digit minute between 00 and 59 inclusive, such as `15` or `37`
        -   **a**: any of `A`, `a`, `AM`, or `am` for AM \(morning\) or any of `P`, `p`, `PM`, or `pm` for PM \(afternoon\)
5.  Create your new user permission crawl by selecting the appropriate option.

    -   If you skipped step [4](create-user-mapping-crawl-external-content-connector.md#schedule-crawl), select **Crawl user permissions**.
    -   If you selected the **Make recurring** option in step [4](create-user-mapping-crawl-external-content-connector.md#schedule-crawl), select **Create user crawl schedule**.

## Result

If you skipped step [4](create-user-mapping-crawl-external-content-connector.md#schedule-crawl), your new user permission crawl is added to the system's crawl queue. The system runs your crawl when it has resources available to do so.

If you selected the **Make recurring** option in step [4](create-user-mapping-crawl-external-content-connector.md#schedule-crawl), your new crawl appears in the Crawl schedules list in the external content connector editor's Create crawls tab.

## What to do next

You can monitor your user permission crawl's status or review its results using the crawl history and analytics. For details on these metrics, see [Review crawl history for an external content connector](review-crawl-ext-cont-connector.md) and [Review user permissions for an external content connector](review-usr-maps-ext-cont-connector.md).

If you need to cancel your running user permission crawl, see [Cancel a running external content connector crawl](cancel-ext-cont-connector-crawl.md).

**Parent Topic:**[Crawling content with External Content Connectors](../concept/using-ext-cont-connectors.md)

