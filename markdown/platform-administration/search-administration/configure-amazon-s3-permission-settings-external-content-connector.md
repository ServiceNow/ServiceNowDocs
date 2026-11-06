---
title: Configure permission mode and user mapping settings for an Amazon S3 external content connector
description: Select the permission mode that controls which users can see content crawled by an Amazon S3 external content connector, and specify user mapping if needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/configure-amazon-s3-permission-settings-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 3
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Amazon S3 external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure permission mode and user mapping settings for an Amazon S3 external content connector

Select the permission mode that controls which users can see content crawled by an Amazon S3 external content connector, and specify user mapping if needed.

## Before you begin

A connector administrator must have already created the Amazon S3 external content connector that you need to configure. To learn about this procedure, see [Create an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-ext-cont-connector-amazon-s3.md).

To use the standard user permission crawl or the all retrieved users group, your AWS administrator must have granted the connector's Identity and Access Management \(IAM\) user the permissions that the mode requires. To learn which permissions each mode requires, see [AWS permissions required for Amazon S3 external content connector permission modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-required-permissions-external-content-connector.md).

Role required: sn\_ext\_conn.xcc\_admin, plus ais\_high\_security\_admin to modify user settings

## About this task

The permission mode determines how the connector assigns access permissions to the content items it indexes. To learn about the available modes and choose the right one for your source system, see [Amazon S3 external content connector permission modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-permission-modes-external-content-connector.md).

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Amazon S3 external content connector whose settings you need to modify.

3.  In the connector editor's **Settings** tab, select **User mapping settings**.

4.  Select the permission mode for the connector.

    -   To use the standard user permission crawl, clear the **Override all document permissions** option.
    -   To use a connector-created group of all retrieved users, select the **Override all document permissions** option, then select **All Mapped Users**.
    -   To make all crawled content visible to users in an existing ServiceNow AI Platform group, select the **Override all document permissions** option, then select **Existing SN Group**, then select the group.
5.  If you're using the standard user permission crawl or the connector-created group, review how the connector maps IAM users to users in your instance.

    In the Map from Amazon S3 section, the connector identifies each IAM user by the user name portion of the user's Amazon Resource Name \(ARN\), which is the final element in the ARN path. For example, for the ARN `arn:aws:iam::123456789012:user/engineering/alice.smith`, the identifier is `alice.smith`. The connector treats roles as groups.

    By default, the connector compares this identifier with the email field of the User \[sys\_user\] table. If your instance identifies users differently, select a different field in the Map to ServiceNow section, or use a custom script to transform the identifier. As an example, if your instance users have email-based user names, you might append your domain name to the identifier:

    ```javascript
    var mapSourceUser = function(sourceUserValue) {
      return sourceUserValue + "@example.com";
    }
    
    mapSourceUser(sourceUserValue);
    ```

    For details about the mapping settings, the custom script, and testing your settings, see [Configure user mapping settings for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-user-mapping-settings-external-content-connector.md).

6.  If you selected the **Override all document permissions** option, select the **I agree to the following disclaimer** option.

7.  Select **Save and validate**.


## Result

The Amazon S3 external content connector is updated with your permission settings.

## What to do next

Run a new content crawl for your connector to retrieve permissions for content items.

If you selected the standard user permission crawl or the connector-created group, create and run a user permission crawl for the connector to retrieve IAM users and groups from your source system. To learn about creating and running user permission crawls, see [Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md).

If you selected an existing group, you don't need to run a user permission crawl.

**Parent Topic:**[Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-external-content-connector.md)

