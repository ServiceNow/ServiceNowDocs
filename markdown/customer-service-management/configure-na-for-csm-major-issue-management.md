---
title: Configure Now Assist for CSM Major Issue Management
description: As an admin, you can customize Major Issue Management detection to match the needs of your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/configure-na-for-csm-major-issue-management.html
release: australia
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 2
breadcrumb: [Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure Now Assist for CSM Major Issue Management

As an admin, you can customize Major Issue Management detection to match the needs of your organization.

The Now Assist for CSM Major Issue Management feature is delivered by the `com.sn_csm_mim_gen_ai` plugin and runs on a Flow Designer flow called **Major case agentic workflow**. When the flow triggers on a new case, it invokes the **Major Cases Similarity Search** Now Assist skill, evaluates the results, and updates the case record with a suggested major case link.

To activate Now Assist for CSM Major Issue Management, complete the following high level steps:

**Note:** The flow is **inactive** by default. Even if the AI skill is activated, no AI detection runs on new cases until the **Major case agentic workflow** flow is activated.

1.  Activate the **Major Cases Similarity Search** AI skill and confirm its access roles.
2.  Activate the **Major case agentic workflow** flow and edit its trigger conditions to control which cases the AI detection runs against \(for example, restrict by category, account, or product in addition to the default priority and parent conditions\).
3.  Extension point script include: Override detection parameters — similarity thresholds, search profiles, maximum result counts, and additional match field filters — by extending `NowAssistMajorIssueExtPointImpl`.

## What you can configure

-   Which cases the AI detection evaluates \(trigger conditions\)
-   How strict the similarity matching is \(similarity thresholds\)
-   How many similar cases the AI returns \(maximum result counts\)
-   Which AI search profiles are used \(which case fields are searched and how they are weighted\)
-   Additional exact-match field filters layered on top of the similarity search \(for example, restrict matches to cases on the same account or product\)
-   The minimum number of similar non-major cases required before a new major case is auto-proposed
-   Custom eligibility rules for which cases qualify \(override `isValid()`\)

**Related topics**  


[Install Now Assist for CSM Major Issue Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/install-now-assist-for-csm-major-issue-management.md)

[Activate Now Assist for CSM Major Issue Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-na-csm-major-issue-management.md)

[Now Assist for CSM Major Issue Management Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/na-for-csm-mim-properties.md)

