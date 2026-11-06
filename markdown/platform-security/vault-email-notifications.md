---
title: ServiceNow Vault email notifications
description: ServiceNow Vault sends emails to users who have the admin role to help them get started and report how much of their sensitive data ServiceNow Vault protects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/vault-email-notifications.html
release: australia
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [vault email notifications, welcome email, vault coverage report, vault onboarding]
breadcrumb: [Exploring ServiceNow Vault, ServiceNow Vault]
---

# ServiceNow Vault email notifications

ServiceNow Vault sends emails to users who have the admin role to help them get started and report how much of their sensitive data ServiceNow Vault protects.

## Recipients of ServiceNow Vault emails

Only users who have the admin role receive ServiceNow Vault emails.

## Types of ServiceNow Vault emails

<table id="table-vault-email-notifications"><thead><tr><th>

Email

</th><th>

When it's sent

</th><th>

What it contains

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Welcome to ServiceNow Vault

</td><td>

Once, after ServiceNow Vault is installed on an instance that has a ServiceNow Vault entitlement. The instance checks for the entitlement every 12 hours and sends the email the first time it finds one.

</td><td>

-   Confirmation that ServiceNow Vault is active on your instance
-   The ServiceNow Vault capabilities and what each one does
-   A notice that a sample data discovery scan has started on your instance
-   A link to the ServiceNow Vault Welcome Guide on the ServiceNow Community

</td><td>

**Go to Vault console** opens the [ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/vault-dashboard.md).

</td></tr><tr><td>

Data Discovery findings

</td><td>

After the default Data Discovery scan finishes. The default scan typically runs on the first Saturday after ServiceNow Vault is installed.

</td><td>

-   The number of sensitive matches found and the number of tables scanned
-   Scan details, including the scan type and the scan duration
-   Each table where sensitive data was found and the columns with findings in that table

</td><td>

**Review your findings** opens the scan findings for the Data Discovery job.

</td></tr><tr><td>

Vault coverage report

</td><td>

On the last Monday of every month, if Data Discovery has found at least one sensitive column on your instance.

</td><td>

-   The percentage of sensitive columns that a ServiceNow Vault policy covers
-   The number of covered columns out of the total number of sensitive columns
-   The number of tables and data patterns scanned
-   The configuration status of each ServiceNow Vault capability
-   The biggest coverage gaps

</td><td>

**Go to Vault console** opens the [ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/vault-dashboard.md).

</td></tr></tbody>
</table>**Parent Topic:**[Exploring ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/exploring-servicenow-vault.md)

