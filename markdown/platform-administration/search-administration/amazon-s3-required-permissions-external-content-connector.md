---
title: AWS permissions required for Amazon S3 external content connector permission modes
description: The Identity and Access Management \(IAM\) user for an Amazon S3 external content connector requires Amazon S3 and IAM permissions that depend on the permission mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/amazon-s3-required-permissions-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Amazon S3 external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AWS permissions required for Amazon S3 external content connector permission modes

The Identity and Access Management \(IAM\) user for an Amazon S3 external content connector requires Amazon S3 and IAM permissions that depend on the permission mode.

## Permissions by mode

Grant the permissions in the following table to the Identity and Access Management \(IAM\) user whose access key the connector uses. To learn how to create this user and its policy, see [Configure Amazon S3 for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-amazon-s3-external-content-indexing.md). To learn about the modes, see [Amazon S3 external content connector permission modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-permission-modes-external-content-connector.md).

<table id="table_required_permissions"><thead><tr><th>

Permission mode

</th><th>

Required permissions

</th></tr></thead><tbody><tr><td>

All modes

</td><td>

-   `s3:GetBucketLocation`
-   `s3:GetObject`
-   `s3:ListBucket`

</td></tr><tr><td>

Standard user permission crawl

</td><td>

The permissions for all modes, plus the following permissions:-   `iam:GetGroup`
-   `iam:GetGroupPolicy`
-   `iam:GetPolicy`
-   `iam:GetPolicyVersion`
-   `iam:ListAttachedGroupPolicies`
-   `iam:ListGroupPolicies`
-   `iam:ListGroups`
-   `iam:ListRoles`
-   `iam:ListUsers`
-   `s3:GetBucketPolicy`

</td></tr><tr><td>

User permission crawl with a connector-created group of all retrieved users

</td><td>

The permissions for all modes, plus `iam:ListUsers`.

</td></tr><tr><td>

No user permission crawl with an existing group

</td><td>

The permissions for all modes. This mode requires no IAM permissions.

</td></tr></tbody>
</table>**Important:** In the standard user permission crawl, if the connector can't list IAM users and roles, it can't resolve the principals in a bucket policy. In that case, the connector indexes no content from the affected buckets. If the connector can't read the policy for a bucket, for example because `s3:GetBucketPolicy` is denied, no user can see content items indexed from that bucket.

**Parent Topic:**[Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-external-content-connector.md)

**Related topics**  


[Amazon S3 external content connector permission modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-permission-modes-external-content-connector.md)

[Configure Amazon S3 for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-amazon-s3-external-content-indexing.md)

