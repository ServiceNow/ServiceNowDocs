---
title: Define a crawl schedule for an external content connector
description: Keep your search index up to date by scheduling regular document and user mapping crawls for your external content connector. Scheduled crawls can run daily or on selected days of the week, starting at a time that you specify.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-05"
reading_time_minutes: 3
breadcrumb: [Crawl, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define a crawl schedule for an external content connector

Keep your search index up to date by scheduling regular document and user mapping crawls for your external content connector. Scheduled crawls can run daily or on selected days of the week, starting at a time that you specify.

## Before you begin

Role required: ais\_admin

## About this task

Scheduled crawls retrieve updated data from an external content connector's data source on a regular basis, either daily or weekly. For weekly crawls, you can specify which days of the week you want crawls to run on. For either type of crawl, you can set the time of day at which you want the connector to begin crawling.

**Note:** To prevent excessive load on your instance, the External Content Connectors application only allows a maximum of five crawls to run simultaneously, no matter how many connectors you have created. Both content crawls and user permission crawls count against this limit. For best performance, run and schedule your external content connector crawls so that they don't overlap.

To ensure that all relevant updates from the data source are sent to the AI Search index, configure at least one scheduled document crawl and one user mapping crawl per external content connector.

**Note:** Some external content connectors have schedules configured automatically by the system. You can't create or edit schedules for these connectors.

-   Predefined web sources external content connector
-   ServiceNow documentation external content connector

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the connector that you want to schedule a crawl for.

3.  In the connector editor's Create crawls tab, select **Create schedule**.

4.  In the Create crawl schedule dialog box's Crawl setting section, select one of the following document crawl types:

    -   To crawl your entire source system, starting at its root URL, select **Full document crawl**.
    -   To crawl a subset of your source system, starting from a point you specify and only retrieving documents located beneath that starting point, select **Partial document crawl**.
    -   To crawl users and group memberships from your source system, select **User mapping crawl**.

        **Note:** Some external content connectors don't retrieve user and group access permissions. You can't run user mapping crawls for these connectors.

        -   Predefined web sources external content connector
        -   ServiceNow documentation external content connector
        -   Slack external content connector
        The Atlassian Confluence Cloud external content connector only maps permissions for Confluence Cloud users who have made their email addresses visible to all users. To allow user mapping, each Confluence Cloud user must set their own email visibility to **Anyone** as explained in the [https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/](https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/) Atlassian support resource.

5.  If you selected **Partial document crawl** in step [4](run-doc-crawl-ext-cont-connector.md#select-ext-cont-doc-crawl-type), select **Refresh start points**, wait for the **Select start points** list to populate, then select the point where you want the partial crawl to start.

    **Note:** Refreshing the start point list requires the connector to retrieve data from the external data source and may take a minute or two.

6.  In the Create crawl schedule dialog box's Schedule section, select **Daily** or **Weekly** as the frequency for the scheduled crawl.

7.  If you selected **Weekly** in step [6](define-schedule-ext-cont-connector.md#select-schedule-crawl-frequency), select the days of the week that you want the scheduled crawl to run on.

8.  Specify when you want the system to run the scheduled crawl by entering its start time and time zone.

    The start time should be in **hh:mm a** format, where the format parameters have the following values:

    -   **hh**: a one- or two-digit hour between 0 and 12 inclusive, such as `5` or `11`
    -   **mm**: a two-digit minute between 00 and 59 inclusive, such as `15` or `37`
    -   **a**: any of `A`, `a`, `AM`, or `am` for AM \(morning\) or any of `P`, `p`, `PM`, or `pm` for PM \(afternoon\)
9.  Select **Create**.


**Parent Topic:**[Crawling content with External Content Connectors](../concept/using-ext-cont-connectors.md)

