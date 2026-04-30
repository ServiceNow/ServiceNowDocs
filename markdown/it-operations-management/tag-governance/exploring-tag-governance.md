---
title: Exploring Tag Governance
description: Learn more about Tag Governance reports and discovery.
locale: en-US
release: xanadu
product: Tag Governance
classification: tag-governance
topic_type: concept
last_updated: "2024-10-01"
reading_time_minutes: 3
breadcrumb: [Tag Governance, ITOM Visibility, IT Operations Management]
---

# Exploring Tag Governance

Learn more about Tag Governance reports and discovery.

## Tag Governance overview

Effective tag management improves reporting and overall operations management efficiency. Use the ServiceNow® Tag Governance app to identify on-premises or cloud resources that are inconsistent and don't comply with the tag policies of your organization.

## Tag Governance users

<table id="table_p13_dsn_gcc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tag Governance admin

</td><td>

Responsible for maintaining uniform tag management policies and ensuring resources are properly tagged for visibility, compliance, and cost management.

</td></tr><tr><td>

Report viewer

</td><td>

View-only permissions:-   Monitor reports from audit runs
-   Analyze the data to derive insights to guide actions

</td></tr></tbody>
</table>## Tag Governance workflow

![Tag governance workflow.](../image/tag-gov-workflow.png "Tag Governance workflow")

## Tag Governance benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Implement cloud event processing and configure a tag policy to automatically update cloud resource tags in real time.|[Performing real-time updates to tags for cloud resources](tag-governance-real-time-updates.md)|Cloud admins|
|Tag Governance supports domain separation, allowing you to logically group and segregate data, processes, and administrative tasks into distinct domains. This enables precise control over aspects like user access and data visibility.|[Domain separation and Tag Governance](tag-governance-domain-separation.md)|Cloud admins|
|Review non-compliant CIs flagged by tag audits and resolve them by adding the required tags.|[Preview and remediate tag audit failures](../task/perform-remediations-tag-governance.md)|Tag admins|

## Exploring

-   **[Discovery's contribution to Tag Governance](tag-governance-and-discovery.md)**

    The Discovery and Cloud Discovery features discover all resources in the CMDB as well as cloud resources from cloud providers such as Amazon AWS Cloud, Microsoft Azure Cloud, and Google Cloud Platform \(GCP\).

-   **[Tag Governance dashboard – Overview tab](tag-governance-dashboard-health.md)**

    The **Overview** tab tracks the health and compliance of CIs based on tag audits. Interactive widgets provide information that enables you to view and analyze tag compliance status and the most-used and least-used tags.

-   **[Tag Governance dashboard – Policy View tab](tag-governance-dashboard-policy.md)**

    Use the Policy View tab to view and analyze tag compliance filtered by cloud service account, by tag policy, and by datacenter. Filters enable you to focus your efforts to improve tag compliance.

-   **[Tag Governance dashboard – Efficacy tab](tag-governance-dashboard-efficacy.md)**

    The Efficacy tab displays the results of tag audits as tag health ratings and compliance coverage of CIs. Interactive widgets show tag coverage status and tagging trends over time.


## What to explore next

To learn more about configuring and using Tag Governance, see:

-   [Configuring Tag Governance](configuring-tag-governance.md)
-   [Using Tag Governance](using-tag-governance.md)
-   [Tag Governance reference](reference-tag-governance.md)

