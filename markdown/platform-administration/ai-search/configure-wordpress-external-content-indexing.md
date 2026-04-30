---
title: Configure WordPress for external content indexing
description: Create an admin user and an application password in your WordPress website to allow the WordPress external content connector to access your WordPress content.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-14"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [WordPress external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure WordPress for external content indexing

Create an admin user and an application password in your WordPress website to allow the WordPress external content connector to access your WordPress content.

## Before you begin

You need administrator access privileges for the WordPress website that you want the connector to retrieve content from.

Role required: none

## About this task

The WordPress external content connector retrieves pages and blog posts and their attachments from your WordPress source system using the WordPress REST API.

To allow the connector to access your WordPress source system via the WordPress REST API, you must set an application user name and password in the WordPress Admin dashboard. Your connector admin can use these credentials to configure the WordPress external connector for proper connection to your source system.

## Procedure

1.  Navigate to the WordPress Admin dashboard at `https://<wordpress-site>/wp-admin/`, replacing `<wordpress-site>` with the fully-qualified hostname for your WordPress website.

    For example, if your WordPress website is in the `wordpress.com` domain, you might replace `<wordpress-hostname>` with `example.wordpress.com`. If your WordPress website has its own domain, you might replace `<wordpress-hostname>` with `example-wordpress.com`.

2.  When prompted, log in with your WordPress administrator credentials.

3.  Navigate to **Users**.

4.  Add a new administrator user account:

    1.  Select **Add User**.

    2.  Enter a username and email address for your new user account.

        As an example, you might enter `WP_XCC_admin_user` as the username and `wp-admin@example.com` as the email address.

    3.  Copy the username you entered and record it in a secure location.

        **Important:** Your external content connector admin needs this user name when configuring the WordPress external content connector.

    4.  Replace the auto-generated password for the new user account by selecting **Generate password** or entering a password of your own choice.

    5.  In the Role field, select **Administrator** as the role for the new user account.

    6.  Select **Add User**.

    The new user account appears in the Users list with the administrator role.

5.  Generate an application password for your new administrator user account.

    1.  In the Users list, edit your new administrator user account.

    2.  In the New Application Password Name field, enter a name for the new application password.

        As an example, you might enter `WordPress external content connector app password`.

    3.  Select **Add Application Password**.

        The user editor page displays the new application password.

    4.  Copy the new application password and record it in a secure location.

        **Important:** Your external content connector admin needs this application password when configuring the WordPress external content connector.

    5.  Select **Update User**.


## What to do next

Provide the following items to your connector admin:

-   The URL for your WordPress website.
-   The user name for the administrator user account that you copied in step [4.c](configure-wordpress-external-content-indexing.md#copy-username-step).
-   The application password for the administrator user account that you copied in step [5.d](configure-wordpress-external-content-indexing.md#copy-password-step).

Your connector admin needs these items to configure a WordPress external content connector to retrieve pages and blog posts and security principals from your WordPress source system.

For details on creating and configuring a WordPress external content connector, see [Create a WordPress external content connector](create-ext-cont-connector-wordpress.md).

**Parent Topic:**[WordPress external content connector](../concept/wordpress-external-content-connector.md)

