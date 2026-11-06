---
title: Security findings
description: Provides Machine Identity security score and findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/identity/security-score.html
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Exploring Machine Identity Console, Machine Identity Console, Identity]
---

# Security findings

Provides Machine Identity security score and findings.

## Machine identity security score and findings

The security score is displayed for following security findings. You can select each findings for learn more.

\[Omitted image "mic-security-findings-landing.png"\] Alt text: Machine Identity security score and findings

|Findings|Description|
|--------|-----------|
|Accounts with no login for 100 days|Findings about the accounts that have not accessed any API in 100 days.|
|Accounts using Basic Authentication|Findings about the accounts that are using username and password for authentication.|
|Integration accounts with Web Service Access disabled|Findings about all the accounts that have WSA disabled.|
|Accounts performing both UI and API logins|Findings about the accounts that are used for both interactive \(UI\) and machine \(API\) logins.|

## Machine identity Security score and findings

The security score is based on the usage and method of machine identities. A lower score indicates a higher risk. You can view the recommendations to take preventive actions for these identities.

## How the score is calculated

The security score is based on the findings listed above. Each active finding category has an equal share of the total impact, which is 100 divided by the number of active categories. Any remainder is assigned to the UI login and integration category.

The score windows are 30 days and 100 days. Scores are computed daily at 00:01 and don't include the current day, so they can be about a day behind the findings list. To turn a finding category on or off, see [Machine Identity Console Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/machine-identity-console-settings.md).

