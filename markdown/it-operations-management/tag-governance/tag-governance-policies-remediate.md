---
title: Tag policies and remediation for AWS
description: Tag audits apply policies to discovered CIs to determine tag compliance; existence of tags, appropriate count of tags, and the presence of specified key-value pairs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/tag-governance/tag-governance-policies-remediate.html
release: zurich
product: Tag Governance
classification: tag-governance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tag Governance reference, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Tag policies and remediation for AWS

Tag audits apply policies to discovered CIs to determine tag compliance; existence of tags, appropriate count of tags, and the presence of specified key-value pairs.

## Tag policies

Run a tag audit to audit discovered CIs for the following tag policy types:

-   Tag Count: Checks CIs for the tag key count that you specify
-   Tag Presence: Checks CIs for the presence of the tag key values that you specify
-   Tag Key &amp; Value: Checks CIs for the presence of key-value pairs that you specify.

Specify string value or tag keys that you are looking for in a comma-separated format in the Tag Presence policy type. You can also specify a number in the Tag Count check policy type to identify CIs with one or more tags. After you run the tag audits, you can view audit results and configure remediation measures that are based on the compliance index quality. Optionally, you can also assign remediation tasks for non-compliant CIs to user groups and users for follow-on tasks.

Auto-remediation works with the Assume Role on AWS to automate the tagging of cloud resources, by following the steps in [Configure temporary credential access for trusted AWS accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/configure-iam-role-aws-account.md).

The Assume Role must have the following permissions \(policy\) for remediation to work:

```
{ 

    "Version": "2012-10-17", 

    "Statement": [ 

        { 

            "Effect": "Allow", 

            "Action": "tag:TagResources", 

            "Resource": [ 

                "arn:aws:ec2:*:*:instance/*", 

                "arn:aws:ec2:*:*:security-group/*", 

                "arn:aws:ec2:*:*:volume/*", 

                "arn:aws:ec2:*:*:vpc/*", 

                "arn:aws:ec2:*:*:subnet/*", 

                "arn:aws:ec2:*:*:network-interface/*", 

                "arn:aws:elasticloadbalancing:*:*:loadbalancer/*", 

                "arn:aws:ec2:*:*:availability-zone/*", 

                "arn:aws:ec2:*:*:public-ip/*", 

                "arn:aws:storagegateway:*:*:gateway/*", 

                "arn:aws:resource-groups:*:*:group/*" 

            ] 

        } 

    ] 

} 
```

**Note:**

While performing tag remediation, if it is found that Discovery is credential-less, MID Server with Tag Management capability is picked. Hence, add Tag Management capability to the correct MID Server with service account IAM role attached. This action is essential because there might be several accounts that IAM role MID Servers must choose from.

For more information, see [contact Customer Service and Support.](https://www.servicenow.com/support/contact-support.html)

**Parent Topic:**[Tag Governance reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/tag-governance/reference-tag-governance.md)

