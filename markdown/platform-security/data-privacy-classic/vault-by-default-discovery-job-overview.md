---
title: Default data discovery job
description: The Vault by Default data discovery job automatically runs on ServiceNow instances. It helps to identify sensitive data in primary sources, providing immediate value for trial and licensed Vault customers without requiring configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/data-privacy-classic/vault-by-default-discovery-job-overview.html
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-11-06"
reading_time_minutes: 2
breadcrumb: [Default data privacy configurations, Data Privacy, Platform Privacy]
---

# Default data discovery job

The Vault by Default data discovery job automatically runs on ServiceNow instances. It helps to identify sensitive data in primary sources, providing immediate value for trial and licensed Vault customers without requiring configuration.

The default initiative removes setup barriers by introducing an automatic data discovery job that runs out-of-the-box on all trial and licensed Vault instances. This job scans the three primary sources of accidental PII exposure on the ServiceNow platform and delivers findings directly to administrators.

## Sample scan type specifications

The Sample scan type is a specialized discovery job scan type that is:

-   **Bounded:** Scans only the first 1,000 records OR records from the last 30 days \(whichever limit is reached first\)
-   **Performance optimized:** Designed to complete quickly on instances of any size without performance impact
-   **Pre-configured:** Includes predefined patterns for journal fields, free text fields, and OOTB regex patterns for common PII types

This design ensures the first scan completes quickly and delivers immediate value without overwhelming the administrator with results.

## Customer eligibility and job execution

The default discovery job execution depends on customer type and Vault license status:

|Customer Type|License Requirement|Job Trigger Point|Target Instance|
|-------------|-------------------|-----------------|---------------|
|Trial Customer \(30-day\)|None \(trial period\)|Upon trial activation|Sub-prod instance|
|New Licensed Customer|Active Vault license required|Upon license activation|Production or designated instance|
|Existing Licensed Customer|Active Vault license required|Upon upgrade to required Store App version|Existing instance|

## Default discovery job policy

The default discovery job uses a pre-configured global policy that includes:

-   **Target data sources:** Journal fields, free text fields, and fields matching OOTB regex patterns
-   **Sensitive data patterns:** Out-of-the-box patterns for credit cards, social security numbers, email addresses, phone numbers, and other common PII types
-   **Global scope:** The policy is created in global scope, allowing customers to view, edit, and extend it as needed
-   **Non-destructive:** The default policy does not modify or delete any data; it only identifies and reports on sensitive data presence

Customers can customize this policy or create additional discovery jobs with different patterns and scope as their requirements evolve.

## Limitations and considerations

-   **Pattern accuracy:** OOTB regex patterns may have false positives or false negatives depending on data format and specificity
-   **Non-configurable timing:** The default discovery job runs automatically on a fixed schedule; administrators cannot manually trigger the initial job
-   **Email notifications:** The Sensitive Data Visibility report is sent to users with `admin` and `data_discovery_admin` roles. It provides a summary of sensitive data in the free text and journal fields across the scanned tables and columns

