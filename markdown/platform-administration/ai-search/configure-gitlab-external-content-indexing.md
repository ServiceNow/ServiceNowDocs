---
title: Configure GitLab for external content indexing
description: Create a personal access token for a group owner user account on GitLab.com to allow the GitLab external content connector to access your GitLab source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [GitLab external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure GitLab for external content indexing

Create a personal access token for a group owner user account on GitLab.com to allow the GitLab external content connector to access your GitLab source system.

## Before you begin

You need login credentials for the group owner user account in your organization's GitLab.com instance.

Role required: none

## About this task

The GitLab external content connector retrieves content from your GitLab.com source system using the GitLab API and a personal access token with the **read\_api** scope configured for the user account that owns all top-level groups you want to crawl. The connector uses this personal access token to impersonate the specified user when retrieving searchable content and security principals from your GitLab.com source system.

Your ServiceNow AI Platform instance admin needs this personal access token to configure the GitLab external content connector for proper connection to your GitLab.com source system.

## Procedure

1.  Log in to [https://gitlab.com/](https://gitlab.com/) as the user that owns all top-level groups you want to retrieve searchable content from.

2.  In the menu, select your avatar, then select **Edit profile**.

    ![Edit profile link in user menu on GitLab.com.](../image/gitlab-edit-profile.png)

3.  Select **Access tokens**, then select **Add new token**.

    ![Access tokens page on GitLab.com showing Add new token button.](../image/gitlab-access-tokens-add-new-token.png)

4.  Enter a name, optional description, and expiration date for your new personal access token.

    **Note:** If you don't enter an expiration date, the token's expiration date is automatically set to 365 days later than the current date.

5.  Select the **read\_api** scope for your new personal access token.

6.  Select **Create token**.

    ![Personal access tokens form on GitLab.com showing token name, description, expiration date, and scopes plus Create token button.](../image/gitlab-access-tokens-create-personal-access-token.png)

7.  When prompted, select the copy icon ![](../image/gitlab-copy-personal-access-token-icon.png) to copy your new personal access token, then save it in a secure location.

    ![Access tokens page on GitLab.com showing new personal access token.](../image/gitlab-access-tokens-copy-new-personal-access-token.png)

    **Important:** Your connector admin needs this personal access token to create a GitLab external content connector. You won't be able to access the token again after creating it.


## What to do next

Provide the following items to your connector admin:

-   The URL for your GitLab instance. This is typically [https://gitlab.com/](https://gitlab.com/).
-   The personal access token for the group owner user that you copied in step [7](configure-gitlab-external-content-indexing.md#copy-personal-access-token).

Your connector admin needs these items to configure a GitLab external content connector to retrieve searchable content and security principals from your GitLab.com instance.

For details on creating and configuring a GitLab external content connector, see [Create a GitLab external content connector](create-ext-cont-connector-gitlab.md).

**Parent Topic:**[GitLab external content connector](../concept/gitlab-external-content-connector.md)

