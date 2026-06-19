---
title: Define policies in Digital Product Release
description: Define policies to automate the release workflow based on the different states of the release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/digital-product-release/dpr-create-policy-admin.html
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 2
breadcrumb: [Configure, Digital Product Release, IT Service Management]
---

# Define policies in Digital Product Release

Define policies to automate the release workflow based on the different states of the release.

## Before you begin

Role required: sn\_dpr\_model.release\_admin

## About this task

The policies are defined using ServiceNow® Policy as Code Engine \(PaCE\), so make sure you’re familiar with the basics. For more information, see .

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the policy administration icon \(\[Omitted image "dpr-icon-policy-admin.png"\] Alt text: Policy administration icon.\).

3.  Create a policy or update an existing one.

    -   To create a policy, select **New**.

        For more information on creating a policy, see .

    -   To modify an existing policy, open the policy from the list.
    A policy is created in the inactive state and a draft version of the policy is added.

4.  Select the **Version** tab and open the draft version.

5.  On the Version record form, select the **Policy Builder** tab to write the policy.

    1.  On the **Define Variables** pane, use API variables, config parameters, record references, and data collectors to write your policy.

    2.  Process data from the DevOps application data model related to the product using the base system data collectors.

        The data collectors collect inputs by processing data from ServiceNow or an external data source to provide an output. The output can be used in the policy logic to take a decision. For more information, see [Digital Product Release data collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-product-release/dpr-data-collector.md).

6.  Test your policy in the **Test Playground** tab.

    For more information, see .

7.  Select **Save** to save the policy version.

    You can also save the version as a template by selecting the **Save as template**.

8.  To enable exceptions for the policy for temporarily overriding the policy failure status for specific use cases, select more actions icon \(\[Omitted image "dpr-icon-more-actions.png"\] Alt text: More actions icon.\) and then select **Enable exceptions**.

    **Note:** This option is only available when GRC: Policy and Compliance Management is installed.

    The **Exceptions** tab displays. You can view a list of exceptions requested for this policy, including their active status and expiry. You can withdraw or extend any existing exceptions for the policy.

9.  Select **Publish** to publish the policy version and make it available for use.

10. In the Publish draft dialog box, select **Activate this policy** to also activate the policy along with publishing the version.


## Result

The policy version is updated as Current and is used the next time the policy is invoked.

For more information, see .

