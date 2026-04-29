---
title: General guidelines for RSS feeds
description: When an RSS feed isn't working, common errors or issues often stem from improper formatting, server issues, or misconfiguration. An RCM administrator can remediate some of the common errors that users may encounter.
locale: en-US
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Overview of RSS feeds, Integrate, Regulatory Change Management, Governance, Risk, and Compliance]
---

# General guidelines for RSS feeds

When an RSS feed isn't working, common errors or issues often stem from improper formatting, server issues, or misconfiguration. An RCM administrator can remediate some of the common errors that users may encounter.

## Overview of common issues in RSS feeds

RSS issues often arise from invalid XML syntax, incorrect URLs, server or authentication problems, caching, incompatible media, outdated standards, size limits, encoding errors, or security and access restrictions. Here’s a list of common problems that users may encounter and their general guidelines to help you get started.

-   **Feed syntax errors**

    The RSS feed XML isn’t properly formatted, leading to parsing errors. To remediate this issue, perform the following checks because as per RSS Standards, all RSS feed files must conform with XML specifications:

    -   Validate the RSS feed using tools like W3C feed validation service.
    -   Check for missing or mismatched tags, unescaped characters, or improperly nested elements
-   **Incorrect or outdated feed URL**

    This issue occurs when the URL for the RSS feed is incorrect or has changed. To resolve this issue, verify the feed URL and update it if necessary.

-   **Server issues**

    This issue occurs when the server hosting the RSS feed is down or slow to respond. To resolve this issues, check server logs, ensure uptime, and optimize performance

-   **HttpException: Session contains no certificates - Untrusted**

    This happens when the feed source is pointing to a site for which the certificates are expired. This must be handled by the customer. The customer can validate the source URLs in online validation portals. For example, [https://validator.w3.org/feed/](https://validator.w3.org/feed/) &amp; [https://www.sslshopper.com/ssl-checker.html](https://www.sslshopper.com/ssl-checker.html)

-   **Response size exceeds limit**

    This happens when the response from REST step is more than what is allowed. You can try increasing the limit by updating the value of property “glide.pf.rest.response\_payload\_max\_size". Refer to [https://www.servicenow.com/docs/bundle/xanadu-build-workflows/page/administer/flow-designer/reference/rest-request-action-designer.html](https://www.servicenow.com/docs/bundle/xanadu-build-workflows/page/administer/flow-designer/reference/rest-request-action-designer.html) for more information.

-   **Response status is 404**

    This error occurs when the website doesn't function.

-   **Other issues**

    Upgrade your instance and debug by looking at the execution logs for the flow titled **Pull RSS feed into regulatory change**.


**Parent Topic:**[RSS feeds overview](rss-feeds.md)

