---
title: Set up credential record for Amazon SQS
description: Create a credential record on your ServiceNow instance for accessing the Amazon AWS.Specify whether record is for a host, instance, server, custom application, or account
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/set-up-credential-record-for-amazon-sqs.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up Amazon SQS spoke, Amazon SQS Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up credential record for Amazon SQS

Create a credential record on your ServiceNow instance for accessing the Amazon AWS.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Amazon SQS spoke plugin.
-   Ensure that you have access to the Amazon Web Services\(AWS\) account to create access keys and secure access keys.
-   Role required: admin

## Procedure

1.  Create an access key and a secure access key in the Amazon AWS.

    1.  Log in to Amazon Web Services.

    2.  On the console home page, in the search field, enter `Users`.\[Omitted image "amazon-sqs-enter-users.png"\] Alt text: Search field on Amazon AWS home page.

        \[Omitted image "amazon-sqs-enter-users.png"\] Alt text: Search field on Amazon AWS home page.

    3.  Select Users from the search results.\[Omitted image "amazon-sqs-search-results-user.png"\] Alt text: Users option in search results.

        \[Omitted image "amazon-sqs-search-results-user.png"\] Alt text: Users option in search results.

    4.  In the Users field, enter the user name under which you want to create the access and secret access keys or select a user name under the User name column.

    5.  Select the Security credentials tab.

        \[Omitted image "amazon-sqs-click-security-cred-tab.png"\] Alt text: Security credentials tab.

    6.  Under the Access keys heading, select **Create access key**.\[Omitted image "amazon-sqs-create-access-key.png"\] Alt text: Create access key button.

    7.  Under the Access key best practices &amp; alternatives heading, select Other.

        \[Omitted image "amazon-sqs-select-other.png"\] Alt text: Other option.

    8.  Select **Next**.

    9.  In the Description tag value field, enter a custom tag that describes the access key.

    10. Select **Create access key**.

    11. Copy the access key and the secret access key, and store at a secure place.

        The credential record you set up on your ServiceNow instance requires the access and secret access keys.

        \[Omitted image "amazon-sqs-copy-access-key.png"\] Alt text: Copy access key button.

    12. To view the secret access key, select **Show**.

    13. Select **Done**.

2.  Create the credential record.

    1.  Log in to your ServiceNow instance.

    2.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    3.  Select the Amazon SQS connection and credential alias.

        The alias becomes available as a base system component when you install the Amazon SQS spoke plugin.

    4.  Under the Credentials tab, select **New**.

        \[Omitted image "amazon-sqs-create-cred.png"\] Alt text: New button for creating credential record.

    5.  Under the heading What type of Credentials would you like to create?, select AWS Credentials.

    6.  Fill the form.

        |Field|Description|
        |-----|-----------|
        |Name|Custom name of the credential record.|
        |Active|If the field is selected, you can use this record to access the Amazon SQS.|
        |Access Key ID|Enter the access key you had generated on Amazon AWS.|
        |Secret Access Key|Enter the secret access key you had generated on Amazon AWS.|
        |Authentication Algorithm|Algorithm used to authenticate credential record. To select the algorithm, select\[Omitted image "magnify-icon.png"\] Alt text: Lookup list icon. and from the list, select Amazon SQS.|

    7.  Select **Submit**.


