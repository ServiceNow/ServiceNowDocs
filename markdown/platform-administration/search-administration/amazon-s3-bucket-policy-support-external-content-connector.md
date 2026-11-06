---
title: Amazon S3 bucket policy elements supported by the external content connector
description: In a standard user permission crawl, the Amazon S3 connector evaluates only the policy elements listed here. It doesn't index content items with policy statements that use other elements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/amazon-s3-bucket-policy-support-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: reference
last_updated: "2026-10-27"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Amazon S3 external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Amazon S3 bucket policy elements supported by the external content connector

In a standard user permission crawl, the Amazon S3 connector evaluates only the policy elements listed here. It doesn't index content items with policy statements that use other elements.

## Supported actions and effects

The connector evaluates only the policy statements whose action matches a supported action.

-   Actions: `s3:GetObject` and wildcards such as `s3:Get*`, `s3:*`, or `"*"`.
-   Effects: `Allow` and `Deny`. A `Deny` takes precedence over an `Allow`.

The connector checks a statement for unsupported elements only after it confirms that the statement applies to the content item's resource and to the read action. A statement that uses an unsupported condition under an unrelated action, such as `s3:PutObject`, or that applies to a different prefix, doesn't affect the content item.

## Supported principals

The connector resolves principals against the Identity and Access Management \(IAM\) users and roles that it crawls.

-   User and role Amazon Resource Names \(ARNs\): The connector grants access to the named user or role.
-   Wildcard principal \(`"*"`\): The connector grants access to the identities it crawled in your AWS account, not to everyone in ServiceNow AI Platform.
-   Account root \(`arn:aws:iam::<account>:root`\): The connector grants access to the crawled users of that account. Account roots from other accounts don't grant access to anyone, because the connector doesn't retrieve the identities of other accounts.

When many users need access to a content item, create an IAM role for the group of users and grant access to the role instead. This approach lists one role in the bucket policy, instead of many individual IAM users.

## Supported condition keys

The connector supports only condition keys whose value follows from the crawled principal, with no extra AWS call.

|Condition key|Value the connector uses|
|-------------|------------------------|
|`aws:PrincipalArn`|The ARN of the user or role. The connector normalizes an assumed-role session ARN to the role ARN.|
|`aws:username`|The IAM user name. This key is absent for roles and for the account root.|
|`aws:PrincipalAccount`|The 12-digit account ID, parsed from the ARN.|
|`aws:PrincipalType`|`User`, `AssumedRole`, or `Account`, derived from the shape of the ARN.|

The connector doesn't support any other condition key. Examples of unsupported keys include `aws:userid`, `aws:PrincipalTag/*`, `aws:ResourceTag/*`, `aws:PrincipalOrgID`, `aws:PrincipalOrgPaths`, network keys such as `aws:SourceIp` and `aws:SourceVpc`, session keys such as `aws:MultiFactorAuthPresent` and `aws:SecureTransport`, time keys such as `aws:CurrentTime`, call-chain keys such as `aws:CalledVia`, and keys that start with `s3:`.

When a condition key doesn't exist for a principal, the result depends on the operator. A positive operator, such as `StringEquals` or `ArnLike`, fails unless you add the `IfExists` suffix, in which case it passes. A negated operator, such as `StringNotEquals` or `ArnNotLike`, passes either way. As an example, `aws:username` doesn't exist for a role, so a statement that requires `aws:username` to equal a value doesn't grant access to roles.

## Supported operators

The connector supports the following operators, each also with the `IfExists` suffix:

-   String operators: `StringEquals`, `StringNotEquals`, `StringLike`, `StringNotLike`.
-   ARN operators: `ArnEquals`, `ArnNotEquals`, `ArnLike`, `ArnNotLike`.

The ARN operators match patterns segment by segment, as AWS does. A `*` doesn't match across a colon, so `arn:aws:iam::*` doesn't match `arn:aws:iam::123456789012:user/alice`.

The connector doesn't support the following operators and qualifiers: `Bool`, `Null`, the `Date` operators, `IpAddress`, `NotIpAddress`, the `Numeric` operators, `StringEqualsIgnoreCase`, `StringNotEqualsIgnoreCase`, and the `ForAnyValue:` and `ForAllValues:` set qualifiers. Condition values that contain a policy variable, such as `${aws:username}`, aren't supported either.

## Unsupported policy elements and messages

The connector doesn't support the `NotPrincipal`, `NotAction`, and `NotResource` elements.

If a policy statement that applies to a content item contains an unsupported element, condition key, operator, or policy variable, the connector doesn't index the content item. It sets the content item to "filtered out" and records one of the following informational messages. The connector doesn't make a best-effort evaluation or a partial evaluation. When the connector can't determine who can see a content item, it indexes nothing, to help avoid exposing a content item to a user who shouldn't see it.

|Message|Meaning|
|-------|-------|
|`unsupported condition: <condition key or element>`|The statement uses a condition key or policy element that the connector doesn't support. For example, `unsupported condition: aws:userid`.|
|`unsupported operator: <operator>`|The statement uses an operator that the connector doesn't support. For example, `unsupported operator: IpAddress`.|
|`unsupported policy variable: <value>`|A condition value contains a policy variable, such as `${aws:username}`.|

A role's trust policy that the connector can't evaluate has a different effect. The connector doesn't filter content items. Instead, it treats the role as having fewer members, or none, and continues the crawl.

**Parent Topic:**[Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-external-content-connector.md)

**Related topics**  


[Amazon S3 external content connector permission modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-permission-modes-external-content-connector.md)

[AWS permissions required for Amazon S3 external content connector permission modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-required-permissions-external-content-connector.md)

