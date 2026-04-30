---
title: GitLab external content connector
description: The GitLab external content connector retrieves issues, wikis, merge requests, tags, branches, and commits from groups, projects, and repositories in your GitLab.com source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-08-04"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# GitLab external content connector

The GitLab external content connector retrieves issues, wikis, merge requests, tags, branches, and commits from groups, projects, and repositories in your GitLab.com source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

## Prerequisites for the GitLab external content connector

## Limitations for the GitLab external content connector

The GitLab external content connector does not retrieve searchable content from personal GitLab.com projects.

When retrieving security principals from your GitLab.com source system, the GitLab external content connector does not support any of these security features:

-   [Custom roles](https://docs.gitlab.com/user/custom_roles/)
-   [Group access tokens](https://docs.gitlab.com/user/group/settings/group_access_tokens/)
-   Users that are not [Enterprise users](https://docs.gitlab.com/user/enterprise_user/)
-   Users with the [Minimal Access](https://docs.gitlab.com/user/permissions/#users-with-minimal-access) role

-   **[Configure GitLab for external content indexing](../task/configure-gitlab-external-content-indexing.md)**  
Create a personal access token for a group owner user account on GitLab.com to allow the GitLab external content connector to access your GitLab source system.
-   **[Create a GitLab external content connector](../task/create-ext-cont-connector-gitlab.md)**  
Create an external content connector to retrieve searchable content and security principals from your GitLab source system.
-   **[Configure crawl settings for a GitLab external content connector](../task/configure-crawl-settings-gitlab-external-content-connector.md)**  
Specify the groups, projects, and repositories you want your GitLab external content connector to crawl. Select the issues, wikis, merge requests, tags, branches, and commits you want the crawl to retrieve and feed to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

