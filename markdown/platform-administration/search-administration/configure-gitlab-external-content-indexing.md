---
title: Configure GitLab for external content indexing
description: Create a personal access token for a group owner user account on GitLab.com to allow the GitLab external content connector to access your GitLab source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/configure-gitlab-external-content-indexing.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [GitLab external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure GitLab for external content indexing

Create a personal access token for a group owner user account on GitLab.com to allow the GitLab external content connector to access your GitLab source system.

## Before you begin

To use the GitLab external content connector, your GitLab plan must satisfy all of these conditions:

-   **Offering**

    You must be using the GitLab.com offering, not GitLab Dedicated or GitLab Self-Managed.

    To learn more about GitLab offerings, see [https://docs.gitlab.com/subscriptions/choosing\_subscription/\#choose-an-offering](https://docs.gitlab.com/subscriptions/choosing_subscription/#choose-an-offering).

-   **Group owner user account**

    You need a GitLab.com user account that owns all the public and private top-level groups you want the external content connector to crawl. The connector impersonates this user when retrieving searchable content, user access permissions, and security principals from your GitLab source system.

-   **Public content requirements**

    Public content you want to retrieve must be in public top-level groups owned by your group owner user.

-   **Private content requirements**

    Private content you want to retrieve must be in a private top-level group on the Ultimate subscription tier. This group must be owned by your group owner user, and you must have configured access permissions for enterprise users in this private group. \(The connector only retrieves user access permissions and security principals for enterprise users.\)

    To learn more about GitLab subscription tiers, see [https://docs.gitlab.com/subscriptions/choosing\_subscription/\#choose-a-subscription-tier](https://docs.gitlab.com/subscriptions/choosing_subscription/#choose-a-subscription-tier). For information about GitLab enterprise users, see [https://docs.gitlab.com/user/enterprise\_user/](https://docs.gitlab.com/user/enterprise_user/).


You need login credentials for the group owner user account in your organization's GitLab.com instance.

Role required: none

## About this task

The GitLab external content connector retrieves content from your GitLab.com source system using the GitLab API and a personal access token with the **read\_api** scope configured for the user account that owns all top-level groups you want to crawl. The connector uses this personal access token to impersonate the specified user when retrieving searchable content and security principals from your GitLab.com source system.

Your ServiceNow AI Platform instance admin needs this personal access token to configure the GitLab external content connector for proper connection to your GitLab.com source system.

## Procedure

1.  Log in to [https://gitlab.com/](https://gitlab.com/) as the user that owns all top-level groups you want to retrieve searchable content from.

2.  In the menu, select your avatar, then select **Edit profile**.

    \[Omitted image "gitlab-edit-profile.png"\] Alt text: Edit profile link in user menu on GitLab.com.

3.  Select **Access tokens**, then select **Add new token**.

    \[Omitted image "gitlab-access-tokens-add-new-token.png"\] Alt text: Access tokens page on GitLab.com showing Add new token button.

4.  Enter a name, optional description, and expiration date for your new personal access token.

    **Note:** If you don't enter an expiration date, the token's expiration date is automatically set to 365 days later than the current date.

5.  Select the **read\_api** scope for your new personal access token.

6.  Select **Create token**.

    \[Omitted image "gitlab-access-tokens-create-personal-access-token.png"\] Alt text: Personal access tokens form on GitLab.com showing token name, description, expiration date, and scopes plus Create token button.

7.  When prompted, select the copy icon \[Omitted image "gitlab-copy-personal-access-token-icon.png"\] Alt text: to copy your new personal access token, then save it in a secure location.

    \[Omitted image "gitlab-access-tokens-copy-new-personal-access-token.png"\] Alt text: Access tokens page on GitLab.com showing new personal access token.

    **Important:** Your connector administrator needs this personal access token to create a GitLab external content connector. You won't be able to access the token again after creating it.


## What to do next

Provide the following items to your connector administrator:

-   The URL for your GitLab instance. This is typically [https://gitlab.com/](https://gitlab.com/).
-   The personal access token for the group owner user that you copied in step [7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-gitlab-external-content-indexing.md).

Your connector administrator needs these items to configure a GitLab external content connector to retrieve searchable content and security principals from your GitLab.com instance.

For details on creating and configuring a GitLab external content connector, see [Create a GitLab external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-gitlab.md).

**Parent Topic:**[GitLab external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/gitlab-external-content-connector.md)

