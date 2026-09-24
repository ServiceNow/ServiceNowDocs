---
title: Data privacy for inbound emails
description: The inbound email channel enables organizations to discover and mask sensitive data in inbound emails through the Data Privacy framework. This replaces the previous approach which used Active Data Patterns with a centralized, streamlined policy-based experience for managing sensitive data in emails.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/inbound-email-channel-overview.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Data Privacy, Platform Privacy]
---

# Data privacy for inbound emails

The inbound email channel enables organizations to discover and mask sensitive data in inbound emails through the Data Privacy framework. This replaces the previous approach which used Active Data Patterns with a centralized, streamlined policy-based experience for managing sensitive data in emails.

The inbound email channel within the Data Privacy module that allows administrators to define and manage policies to detect and redact sensitive data in inbound emails and any associated inbound actions. This requires customers to have the Sensitive Data Redaction for inbound emails plug-in installed on their instance.

## Migration of existing configurations

For customers upgrading to Brazil with existing email redaction configurations:

-   **Automatic migration:** Upon upgrade, existing email redaction configurations are automatically converted into email channel policies.
-   **Pattern preservation:** Active data patterns used in the old plug-in are migrated to the new email channel policy.
-   **Default policy:** If no active patterns exist, a default email policy is created with no patterns, allowing administrators to configure as needed.

Migration is transparent to end users as defined in the policy; masking continues seamlessly after the upgrade.

## Limitations and considerations

-   **Pattern accuracy:** Sensitive data patterns may have false positives or false negatives depending on pattern specificity.
-   **Email attachments:** Masking may not apply to sensitive data within email attachments; verify scope with your team.

