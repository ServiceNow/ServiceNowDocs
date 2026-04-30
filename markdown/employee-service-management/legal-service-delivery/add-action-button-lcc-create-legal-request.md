---
title: Add action button in Legal Counsel Center Classic to create legal request
description: Add a declarative action button in the Legal Counsel Center Classic to easily create a legal request from the workspace and resolve a request without navigating to the Legal Service Portal.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legal Counsel Center Classic, Legal Service Delivery, Employee Service Management]
---

# Add action button in Legal Counsel Center Classic to create legal request

Add a declarative action button in the Legal Counsel Center Classic to easily create a legal request from the workspace and resolve a request without navigating to the Legal Service Portal.

## Before you begin

**Important:**

-   The legacy Legal Counsel Center was renamed as Legal Counsel Center Classic.
-   Legal Counsel Center Classic is being prepared for deprecation. It will be hidden and no longer available for activation for new customers but will continue to work and be supported for existing customers. For enhanced workspace experience, use [Legal Counsel Center](../concept/legal-counsel-center-landing.md). For details, see the Deprecation Process \[KB0867184\] article in the Now Support knowledge base.
-   If you are upgrading Legal Counsel Center Classic to the latest Xanadu release versions, make sure you have first upgraded it to the Washington DC release version of 6.3.8 or 6.4.1.
-   If you are using Legal Counsel Center Classic and want to upgrade to the Xanadu family release, ensure you upgrade to the Washington DC release first.

Ensure the Legal Request Management application is installed and the application scope is set to Legal Simple Contracts.

Role required: sn\_lg\_ops.legal\_user

## About this task

A legal fulfiller adds a declarative button in the Legal Counsel Center Classic to create legal requests. The button allows the fulfiller to create the request from the Legal Counsel Center Classic directly instead of through the Legal Service Portal.

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Actions &amp; Components** &gt; **List Actions**.

2.  Select **New** on the Action Assignments page.

3.  Enter `Sales Contract` in the **Action label** field.

4.  Set the **Implemented as** field to **Client Action**.

5.  In the **Specify client action** field, select the **Lookup using list** icon \(![Lookup using list icon](../image/lookup-using-list.png)\).

6.  In the Action Payload Definition form, fill in the details to create a record.

    1.  Select **New**.

    2.  Enter `ITEM_SELECTED` in the **Key** field.

    3.  Select the **Lock** icon \(![Lock icon](../image/lock.png)\) to unlock the **Applicable To** field.

        Enter the details in the **Applicable To** field to define the location where the action payload is applicable.

    4.  Enter `List` in the **Select target record** field.

    5.  Enter `{"table":"sc_cat_item","row":{"intake form sys_id":{"value":"72ba83d1b35313007a6de81816a8dc54"}},"parent_table":"{{parentTable}}","additional_data":{"query":"{{query}}"}}` in the Payload field.

        The required data is for a legal request sent to the back-end from the workspace.

    6.  On the form, fill in the remaining fields.

        |Field|Description|
        |-----|-----------|
        |Label|Display label of the action payload definition.|
        |Description|Description of the action payload definition.|
        |Application|Application scope of the action payload definition. This field is pre-populated.|

    7.  Select **Submit**.

7.  To make the action assignment button available on the Legal Counsel Center Classic, follow the steps.

    1.  In the **Workspace** field, start entering `Legal` and select **Legal Counsel Workspace** from the list.

    2.  In the **Table** field, search for `Legal Request` in the drop-down list, and select **Legal Request \(sn\_lg\_ops\_request\)**.

    3.  Select **Submit**.

8.  Move the action assignment button to the **New** button drop-down list in the Legal Counsel Center Classic workspace list view.

    1.  Select **Advanced View**.

    2.  In the **Group** field, select the Lookup using list icon \(![Lookup using list icon](../image/lookup-using-list.png)\) and select the **Group By** check box.

    3.  Select **Legal Request Types**

    4.  Select **Update**.


## Result

The new declarative action button is now available for access in the Legal Counsel Center Classic workspace.

