---
title: Install Card Data Security
description: If you have the admin role, you can install the Card Data Security application \(sn\_data\_sec\).
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Install Card Data Security

If you have the admin role, you can install the Card Data Security application \(sn\_data\_sec\).

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Ensure that you're provisioned with our tokenizer service and that you have completed the onboarding procedure. For more information, see [Initial steps to setup schema and connections for Card data security \(KB2238661\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2238661).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Card Data Security application \(sn\_data\_sec\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


## What to do next

After installing Card Data Security, continue setting up the card vault table and connections in our tokenizer service. For more information, see [Create the card vault table in the tokenizer service](../concept/create-tokenization-vault.md) and [Set up connections to the tokenizer service](set-up-outbound-connections.md).

