---
title: Publish a publication
description: Automatically publish a publication with an optional email notification to send to customers.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Targeted communications, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Publish a publication

Automatically publish a publication with an optional email notification to send to customers.

## Before you begin

Role required: sn\_publications.author or sn\_publications.admin

## About this task

Publications are automatically published at the date and time selected in the **Publish Date** field on the Publication form. When creating a publication, set the **Publish Date** and the **Expiry Date** fields to control when the publication is automatically published and expired.

**Note:** A UI action to manually publish a publication is not available out of box. If needed, the system administrator can [Create a UI action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_EditingAUIAction.md) and add it to the Publication form.

When creating a publication, you can also include an optional email notification that is sent to all recipients in the recipients list when the publication is published. In this email notification, all recipients are included in a **bcc** list to maintain privacy.

**Note:** To exclude inactive users from receiving emails, use the condition builder to exclude inactive users from the recipients list.

## Procedure

1.  Navigate to **All** &gt; **Targeted Communications** &gt; **Active Publications**.

2.  Select the desired publication.

3.  View the date in the **Publish Date** field.

    The system automatically publishes the publication on this date and time and sends an email notification to the recipients in the recipients list.

    **Note:**

    -   If the system administrator has configured a UI action, you can use this UI action for manually publishing the publication.
    -   For more info, see [Email templates](https://servicenow.com/docs/bundle/washingtondc-platform-administration/page/administer/notification/concept/c_EmailTemplates.html).

