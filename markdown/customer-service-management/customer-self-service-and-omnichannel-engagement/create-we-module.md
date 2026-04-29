---
title: Create a module
description: Create a module to manage component instances used in a website. You can either create a module or use a prebuilt module and edit it according to requirement.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure module in Web Embeddables, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Create a module

Create a module to manage component instances used in a website. You can either create a module or use a prebuilt module and edit it according to requirement.

## Before you begin

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  Select **Create module**.

    A dialog box appears for data entry.

3.  Enter the following field values.

<table id="table_tll_jp2_5z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of a module.

</td></tr><tr><td>

Description

</td><td>

Description of a module.

</td></tr><tr><td>

External domain

</td><td>

The domain where you want to embed the ServiceNow components.**Note:** If you update this field, review the configuration status of CORS rules and reconfigure them if necessary.

</td></tr><tr><td>

ServiceNow custom domain

</td><td>

Custom domain for your ServiceNow instance. The instance where the ServiceNow components are configured.**Note:** If you update this field, copy and paste the updated global code on your webpages.

</td></tr><tr><td>

Theme

</td><td>

The theme of the module. Selected theme is applied to all components embed on third-party website. You can select a theme from the list. By default, it is set to Coral. For more information on theme, [Create a theme with Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-theme&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Icon

</td><td>

Thumbnail image of a module. User can see this thumbnail when browsing modules from the Web Embeddables admin Experience.

</td></tr></tbody>
</table>4.  Select **Create module**.

    A module is created and appears on your Web Embeddables home page under **Your module** section. Additionally, a default group named Group 1 is automatically created for your module and is visible in the **Components** tab.

5.  On the module page, select the **Edit** to modify the details.

6.  Select Show module action ![Show module action](../image/we-module-delete-icon.png) icon to delete the module.

    **Note:** This action permanently deletes the module and its component instances, and this action can’t be undone. Existing component instances on your website will continue to function. To remove those instances, delete or comment out the embed codes on your webpages.


