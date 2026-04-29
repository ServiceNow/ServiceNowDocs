---
title: Install PPM Collaboration
description: Install the PPM Collaboration \(sn\_ppm\_collab\) application from ServiceNow Store.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Collaborate with your project teams using PPM Collaboration application, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Install PPM Collaboration

Install the PPM Collaboration \(sn\_ppm\_collab\) application from ServiceNow Store.

## Before you begin

-   Complete the following setup checklist for a smooth installation and configuration.

    **Note:** If you are enabling collaboration with Slack, the Slack spoke v2 plugin must be activated. If you are enabling collaboration with Microsoft Teams, the Microsoft Teams Graph and Microsoft Azure AD spokes must be activated. Collaboration cannot be enabled for both Slack and Microsoft Teams for the same project.

    |Setup tasks|Description|
    |-----------|-----------|
    |Verify that the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin is activated.|Navigate to **All** &gt; **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.|
    |Verify that the Slack spoke v2 \(sn\_slack\_ah\_v2\) plugin is activated, for collaboration with Slack.|Navigate to **All** &gt; **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.|
    |Verify that the Microsoft Teams Graph spoke \(sn\_msteams\_ahv2\) plugin is activated, for collaboration with Microsoft Teams.|Navigate to **All** &gt; **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.|
    |Verify that the Microsoft Azure AD spoke \(com.sn.azure\_ad.spoke\) plugin is activated, for collaboration with Microsoft Teams.|Navigate to **All** &gt; **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.|

    **Note:** Activation of the PPM Standard, Microsoft Teams, and Slack spoke plugins on production instances may require separate licenses. Contact ServiceNow Customer Support for details.

-   Ensure that the PPM Collaboration application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## Procedure

1.  Navigate to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9e8488a8c703330024f6612827c2601b/1.0.2?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%26q%3Datlassian%2520jira%2520integration%2520for%2520agile&sl=sh).

2.  In the ServiceNow Store, search for PPM Collaboration.

3.  Select the application tile.

    You can view detailed information about the application. Consider reading the Other Requirements and Dependencies sections, as applicable.

4.  Select **Get** and enter your Now Support login credentials.

5.  Select **Request Install**.

6.  In the **Instance Name** field, enter your details and select **Validate Instance**.

7.  In the **Reason for the Instance** field, enter your details and select **Request**.

    You receive an email with detailed installation instructions.

8.  Log in to the instance on which you want to install the PPM Collaboration application.

9.  Select **System Applications** &gt; **All Available Applications** &gt; **All**.

10. Locate the application using the filter criteria and search bar, select it, and select **Install**.


## Result

The following components are installed with installation of the application:

-   Roles
-   Tables

For more information, see [Components installed with PPM Collaboration](../reference/components-installed-with-ppm-collab.md).

## What to do next

[Setting up PPM collaboration for Slack](../concept/set-up-collab-ppm.md).

**Parent Topic:**[Using Project Management](../../project-management/concept/using-project-management.md)

