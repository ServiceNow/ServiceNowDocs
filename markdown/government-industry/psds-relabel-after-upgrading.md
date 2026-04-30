---
title: Relabel items for public sector use after upgrade
description: After you upgrade your instance for the first time, you can relabel certain items in the CSM Configurable Workspace for public sector use.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Relabel items for public sector use after upgrade

After you upgrade your instance for the first time, you can relabel certain items in the CSM Configurable Workspace for public sector use.

## Before you begin

Role required: admin

## About this task

Certain menus and menu items in the CSM Configurable Workspace are relabeled for public sector use. However, after upgrading your instance, those items revert to the original labels used for Customer Service Management \(CSM\). You can relabel the following items for public sector use by changing them in the UX List Categories for Customer and Service Organizations.

|CSM label|Change to public sector label|
|---------|-----------------------------|
|Accounts|Businesses|
|Consumers|Constituents|
|Internal Business Location|Internal Agency|
|External Business Locations|External Agency|
|Service Organization External Staff|External Staff|

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the Tables context menu, select **Label** and in the **Search** box enter `*UX list` to search for lists, then select the UX List Category record.

3.  In the UX List Category record, scroll down to the Related Links section and select **Show List**.

    1.  In UX List Categories, select the **Customer** record.

    2.  In the UX List Category for Customer form, go to the UX Lists section and select the **Consumers** record.

    3.  In the **Title** field of the UX List Category for Consumers form, change `Consumers` to `Constituents` and select **Update**.

4.  In UX List Categories, select the **Accounts** record.

    1.  In the **Title** field of the UX List Accounts form, change `Accounts` to `Businesses`.

    2.  Select **Update**.

5.  In UX List Categories, select the **Service Organizations** record.

    1.  In the **Title** field of the UX List Service Organizations form, change `Service Organizations` to `Agency`.

    2.  Select **Update**.

6.  In the UX List Category Agency form, go to the UX Lists section and do the following:

    1.  Select the **Internal Business Location** record.

    2.  In the **Title** field of the UX List Internal Business Location form, change `Internal Business Location` to `Internal Agency`.

    3.  Select **Update**.

    4.  Return to the UX Lists section, and repeat steps a through c for the **External Business Location** record.

        In the **Title** field, change `External Business Location` to `External Agency`.

    5.  Return to the UX Lists section and repeat steps a through c for the **Service Organization External Staff** record.

        In the **Title** field, change `Service Organization External Staff` to `External Staff`.


