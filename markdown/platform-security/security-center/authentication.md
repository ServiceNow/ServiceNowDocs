---
title: Authentication metrics
description: View metrics related to authentication on your instance from a dashboard.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-04-21"
reading_time_minutes: 1
breadcrumb: [Security metrics, Security monitoring console, Security Center, Platform Security]
---

# Authentication metrics

View metrics related to authentication on your instance from a dashboard.

This page displays cards with information on metrics related to authentication. Each card displays a trend line for the following metrics:

-   Users enrolled for MFA: Total count of users enrolled to use MFA.
-   Users using MFA bypass: Total count of users who are circumventing multi factor authentication.
-   High privileged non-MFA user: Total count of high-privileged users that are not using MFA.
-   Active MFA users: Total count of MFA users that are active on your instance.
-   Locked out MFA users: Total count of MFA users who are locked out on your instance.
-   Web service account user: Total count of users with web service account only.
-   X509 certificates expiring: Total count of X509 certificates that are expiring in the next 30 days.
-   Biometric scanner/Hardware key users: Total count of users login with biometric scanner or Hardware key.
-   REST API's Without Access Policy: Total count of users login without REST API's Access Policy.
-   Integration Accounts without Web Service Access Only Flag enabled: Total count of users login without Integration Accounts Web Service Access Only Flag enabled.

Select the cards to view the individual metrics page with additional details.

Select the **+Create task** button to create a Security Task related to a metric. For details on Security Tasks, see [Security Tasks](security-task-manager.md).

**Parent Topic:**[Security metrics](sc-metrics.md)

