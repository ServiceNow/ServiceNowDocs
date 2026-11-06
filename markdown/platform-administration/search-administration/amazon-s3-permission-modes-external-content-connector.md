---
title: Amazon S3 external content connector permission modes
description: The Amazon S3 external content connector offers multiple permission modes to control which users can see its crawled content items in AI Search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/amazon-s3-permission-modes-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 5
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Amazon S3 external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Amazon S3 external content connector permission modes

The Amazon S3 external content connector offers multiple permission modes to control which users can see its crawled content items in AI Search applications.

When an Amazon S3 external content connector indexes a content item, it records which users and groups are allowed to see that content item. AI Search uses these permissions to show each user only the search results they have access to in the source system. In standard user permission crawl mode, the connector respects the permission model of your Amazon S3 source system. Two simpler modes are available for use with source systems that have broad content visibility across your organization.

|Mode|How you select it on the user mappings page|What the user permission crawl retrieves|Who can see crawled content|
|----|-------------------------------------------|----------------------------------------|---------------------------|
|Standard user permission crawl|Clear the **Override all document permissions** option.|Identity and Access Management \(IAM\) users, roles, and groups|The users and role groups that the bucket policy grants access to, plus the IAM groups whose policies grant access.|
|User permission crawl with a connector-created group of all retrieved users|Select the **Override all document permissions** option, then select **All Mapped Users**.|IAM users only|Every crawled IAM user, through one group that the connector creates automatically. The connector doesn't evaluate bucket policies.|
|No user permission crawl|Select the **Override all document permissions** option, then select **Existing SN Group** and specify an existing ServiceNow AI Platform group.|Nothing|The members of the group you select.|

**Important:** When you upgrade from a previous release that doesn't support user permissions, your existing Amazon S3 external content connector has no permission mode specified. Until you set one of the listed permission modes for the connector, everyone who has access to your configured AI Search experience can see all content retrieved by the connector. Each content crawl records a warning reminding you to select a permission mode.

For details on setting a permission mode for your connector, see [Configure permission mode and user mapping settings for an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-amazon-s3-permission-settings-external-content-connector.md).

## Standard user permission crawl

In this mode, the connector reads the bucket policy for each bucket and determines which users and groups can read each retrieved content item. A user permission crawl maps each IAM user to a user in your ServiceNow AI Platform instance. For details about mapping, see [Configure user mapping settings for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-user-mapping-settings-external-content-connector.md). The connector also evaluates the identity policies of your IAM groups, so a group that grants read access to objects gives that access to its members even when a bucket has no policy.

If a statement in the bucket policy denies access, the deny takes precedence over any allow.

**Important:** If a bucket has no policy, or the connector can't read its policy, content from that bucket is indexed but not visible to any user. The crawl records a warning that names the bucket. Connectors that indexed content from such buckets before permission modes were available no longer return that content in search results after you select this mode.

If a bucket policy statement that applies to a content item uses a condition or operator that the connector doesn't support, the connector doesn't index that item. Instead, it sets the content item to "filtered out" and records an informational message. To learn which policy elements the connector supports, see [Amazon S3 bucket policy elements supported by the external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-bucket-policy-support-external-content-connector.md).

The connector doesn't read the following sources of access, so content that is available to a user only through them isn't reflected in search permissions:

-   Identity-based policies attached directly to an IAM user
-   Per-object access control lists \(ACLs\) in Amazon S3
-   Access that a user gets by assuming a role through another role \(role chaining\)
-   Access limits specified in service control policies \(SCPs\)

## User permission crawl with a connector-created group of all retrieved users

Use this mode to make all retrieved content items visible to every user that the connector retrieves on its user permission crawl. The connector lists the IAM users in your AWS account, adds all of them to one group that the connector creates, and makes every indexed content item visible to all members of that group. The connector doesn't fetch or evaluate bucket policies in this mode.

If the AWS source system has no IAM users, all content items are filtered out and no one can see the connector's indexed content in AI Search applications.

## No user permission crawl with an existing group

Use this mode when you already have a ServiceNow AI Platform group that contains the users who should see the retrieved content. The connector doesn't run a user permission crawl and doesn't require any IAM permissions. Every indexed content item is visible to the members of the group you select.

Group memberships are synced by a queued event and the **XCC Sync domain-public groups** scheduled job, which runs every 15 minutes by default. Changes to group memberships don't affect visible search results until the scheduled job's next run.

**Parent Topic:**[Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-external-content-connector.md)

**Related topics**  


[Configure permission mode and user mapping settings for an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-amazon-s3-permission-settings-external-content-connector.md)

[Amazon S3 bucket policy elements supported by the external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-bucket-policy-support-external-content-connector.md)

[AWS permissions required for Amazon S3 external content connector permission modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-required-permissions-external-content-connector.md)

[Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-external-content-connector.md)

