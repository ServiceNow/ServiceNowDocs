---
title: Install Now Assist for form generation in Creator Studio
description: Install the Now Assist for Creator application from the ServiceNow Store to get Now Assist in Creator Studio.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring form generation in Creator Studio, Configuring Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Install Now Assist for form generation in Creator Studio

Install the Now Assist for Creator application from the ServiceNow® Store to get Now Assist in Creator Studio.

## Before you begin

Review the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store to learn about dependencies, licensing, and subscription requirements, and release compatibility. Now Assist for Creator installs the Now Assist for form generation in Creator Studio.

Role required: admin

## Procedure

1.  Navigate to the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application on the ServiceNow Store.

2.  On the Now Assist for Creator application page, select **Request App**.

3.  After your request is approved, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

4.  Find the Now Assist for Creator application \(sn\_now\_creator\) by using the filter criteria and search bar.

5.  Verify that Now Assist for Creator is installed:

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features**.

    2.  In the workflow list, select **Creator**.

    3.  On the Service Catalog card, verify that the catalog item generation skill is active.

        **Note:** If the Service Catalog card displays **Not started** or **Inactive** for the catalog item generation skill, you must activate it. To learn more, see [Activate a Now Assist skill](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

        ![Activation of the Catalog item generation skill on the Service Catalog card in the Now Assist Admin console.](../image/crs-now-assist-activate-form-gen-skills.png)

        ![Cards that display the Catalog item generation skill in the Now Assist Admin console.](../image/crs-now-assist-form-gen-skills.png)

    For more information about using the Now Assist Admin console to access information about setting up, configuring, and monitoring Now Assist applications, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).


## What to do next

Grant the now.assist.creator role to the Creator Studio users to create forms using Now Assist in Creator Studio. To learn more, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Creator Studio roles and personas](../reference/roles-creator-studio.md).

**Parent Topic:**[Configuring form generation in Creator Studio](../concept/creator-studio-configure-now-assist.md)

