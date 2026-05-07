---
title: Configure crawl settings for a GitLab external content connector
description: Specify the groups, projects, and repositories you want your GitLab external content connector to crawl. Select the issues, wikis, merge requests, tags, branches, and commits you want the crawl to retrieve and feed to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [GitLab external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a GitLab external content connector

Specify the groups, projects, and repositories you want your GitLab external content connector to crawl. Select the issues, wikis, merge requests, tags, branches, and commits you want the crawl to retrieve and feed to AI Search for indexing.

## Before you begin

A connector admin must have already created the GitLab external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a GitLab external content connector](create-ext-cont-connector-gitlab.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the GitLab external content connector crawls content from all subgroups, projects, and repositories found in top-level groups owned by the GitLab.com user that it's configured to impersonate, and sends all supported content types \(issues, wikis, merge requests, tags, branches, and commits\) to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the subgroups to crawl when running content crawls
-   Inclusion or exclusion filters for the projects/repositories to crawl when running content crawls
-   Inclusion or exclusion filters for the types of content to retrieve from the source system when running content crawls
-   Inclusion or exclusion filters for the branches to retrieve from the source system when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can handle permissions for up to five hundred thousand \(500,000\) users and their groups. If a connector retrieves users in excess of this limit, user and group permissions may not be correctly applied to the connector's retrieved content. As a result, the content may not be searchable.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternatively, if you need a connector to index more than 10,000,000 content items, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the GitLab external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Group filtering** options:

    -   To crawl all subgroups found in top-level groups owned by the connector's impersonated GitLab.com user account, select **Crawl all groups**.
    -   To crawl only a specified set of subgroups found in top-level groups owned by the connector's impersonated GitLab.com user account, select **Include only these groups**, then use the **Add group URLs to include** field and **Add** button to enter URLs for the groups that you want to include in the crawl.

        For example, you might enter `https://gitlab.com/example-dot-com/production` to include only searchable content from the `production` subgroup and all subgroups that it contains.

    -   To crawl all except a specified set of groups found in top-level groups owned by the connector's impersonated GitLab.com user account, select **Exclude only these groups**, then use the **Add group URLs to exclude** field and **Add** button to enter URLs for the groups that you want to exclude from the crawl.

        For example, you might enter `https://gitlab.com/example-dot-com/test-*` to exclude searchable content from all subgroups with names that start with `test-`.

    **Note:** Subgroup inclusion URLs can be specified as prefixes, with the wildcard character `*` at the end of the URL matching any string.

5.  Select one of the following **Project/repository filtering** options:

    -   To crawl all projects and repositories owned by the connector's impersonated GitLab.com user account, select **Crawl all projects/repositories**.
    -   To crawl only a specified set of projects and repositories owned by the connector's impersonated GitLab.com user account, select **Include only these projects/repositories**, then use the **Add project/repository URLs to include** field and **Add** button to enter URLs for the projects and repositories that you want to include in the crawl.

        **Note:** Project and repository inclusion URLs can be specified as prefixes, with the wildcard character `*` at the end of the URL matching any string.

        For example, you might enter `https://gitlab.com/example-dot-com/prod-*` to include only searchable content from projects whose names start with `prod-`.

    -   To crawl all except a specified set of projects and repositories owned by the connector's impersonated GitLab.com user account, select **Exclude only these projects/repositories**, then use the **Add project/repository URLs to exclude** field and **Add** button to enter URLs for the projects and repositories that you want to exclude from the crawl.

        **Note:** Project and repository exclusion URLs can be specified as prefixes, with the wildcard character `*` at the end of the URL matching any string.

        For example, you might enter `https://gitlab.com/example-dot-com/confidential273` to exclude searchable content from the `confidential273` project.

6.  Enable the **Crawl content types** options for the types of content you want to retrieve when you run content crawls.

    The GitLab external content connector supports indexing of searchable content for these content types:

    |Content type|Searchable content indexed|
    |------------|--------------------------|
    |Issues|Issue description|
    |Wikis|MarkDown content converted to HTML \(without attachments\)|
    |Merge requests|Merge request description \(MarkDown\) and discussions|
    |Tags|Tag message|
    |Branches|Commit message of head commit|
    |Commits|Commit message|

    **Important:** The GitLab external content connector doesn't support indexing of searchable content from any of these content types:

    -   Commit, issue, and wiki discussions
    -   Commit diffs
    -   Content from archived groups or projects
    -   Content from groups or projects in the pending deletion state
    -   Content from subgroups of top-level groups that aren't owned by the impersonated GitLab.com user
    -   Content of files attached to issues or merge requests
    -   Content of wiki attachments in formats other than plain text \(.txt\)
    -   Internal or confidential notes in merge request discussions
    -   Repository files
7.  If you included the Branches content type in step [6](configure-crawl-settings-gitlab-external-content-connector.md#select-content-types-step), use the **Add branches to include in regex format** field and the **Add** button to specify Java regular expression patterns matching the names of branches you want to include in content crawls.

    As an example, you might specify `^2025.*$` to include branches with names that start with `2025`, or specify `^.*$` to crawl all branches. To learn about Java regular expression pattern syntax, see [the Javadoc for the java.regex.util.Pattern class](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/regex/Pattern.html).

    **Note:** The branch name expressions **^main$** and **^master$** are included by default. You can't remove these branches from the list.

8.  Select **Save and validate**.


## Result

The GitLab external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your GitLab source system using your modified crawl settings, create and run a one-time content crawl for your GitLab external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[GitLab external content connector](../concept/gitlab-external-content-connector.md)

