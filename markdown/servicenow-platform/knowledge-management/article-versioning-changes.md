---
title: Article versioning changes
description: Article versioning introduces new actions that allow knowledge users to create and revise versions of existing articles. It also introduces new fields and related lists to the Knowledge form, new columns to the Knowledge list, and updates to Knowledge dashboard reports.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Article versioning changes

Article versioning introduces new actions that allow knowledge users to create and revise versions of existing articles. It also introduces new fields and related lists to the Knowledge form, new columns to the Knowledge list, and updates to Knowledge dashboard reports.

## New user actions

As part of creating article versions, users can:

-   Check out a published article and create another version by clicking **Checkout** on the Knowledge form.

    **Note:** Only the author, knowledge base owner, and users with the knowledge\_admin role can edit an article in the Draft state.

-   Recall an article that is being reviewed or scheduled for publish by clicking **Recall** on the Knowledge form.
-   Select a previously published article in the Outdated state and make it the current published version by clicking **Make this current**in the Knowledge form header.

**Note:** To edit a published article without having to create a new version, make sure the **glide.knowman.versioning.enable\_minor\_edits** property is enabled.

## Changes to the Knowledge list

The article versioning feature adds the following to the Knowledge list:

-   The **Version** column displays the article version number. The Knowledge list displays multiple versions of an article.
-   The **Workflow** column includes the new **Outdated** state.

## Changes to the Knowledge form

The article versioning feature adds the following to the Knowledge form:

-   The **Version** field displays the article version number.
-   The **Display number** field displays a combination of the article number and the version number. For example, KB0010004 v1.02. All references to a knowledge article use this display number.
-   The **Base Version** field displays the knowledge article number and version on which the current article is based.
-   The **Revised By** field displays the name of the user who checked out a published article and created a new version.
-   The **Article Versions** related list displays a list of all versions for an article. From this list,you can:
    -   Click the **Version** to view a specific version of an article.
    -   Click the **View Article** related link to see the article page view.

**Note:** If necessary, configure the form to display the fields and the related list.

## Changes to Knowledge modules

The article versioning feature introduces the following Knowledge module changes:

-   **My Knowledge Articles**
    -   For a knowledge user, this module includes records for the articles authored by the user as well as records for each article revised by the user.
    -   For a knowledge reviser, this module includes records for the articles published by the user as well as records for each article revised by the user.
-   **My Flagged**
    -   For a knowledge user, this module includes records for each revision made to articles authored by the user.
    -   For a knowledge reviser, this module includes records for each article revised by the user.

**Note:** Users that have customized these modules do not see these changes.

## Changes to Knowledge Management dashboard reports

The Knowledge Management Overview dashboard reports have been updated to include article versioning-related changes when the Knowledge Management Advanced plugin is activated.

-   Articles Flagged in the Last 30 Days
-   Articles Marked Not Useful in the Last 30 Days
-   Articles Used per Month
-   Knowledge use
-   Knowledge view
-   Knowledge updated in past 30 days
-   Knowledge flagged in past 30 days
-   Knowledge by Workflow state
-   Knowledge created by Author
-   Knowledge created in past 30 days
-   New Knowledge Articles Created in the Last 30 Days
-   Knowledge Ratings for past 30 days

## Versioning information available in the Knowledge Management Service Portal

Knowledge search results show the article number and the version number for each article.

**Note:**

To display the article version number next to the article number in the search results, enable the **glide.knowman.search.show\_article\_number** property in the Knowledge Search Properties section of the Knowledge Management Properties page.

If you are accessing an article from the base system or knowledge service portals using the URL to a KB article, you must also include the article version number in the URL. For example, to access the KB0000005 knowledge article, instead of using the `https://<instance name>/sp?id=kb_article&sys_id=KB0000005` as the URL, you must use `https://<instance name>/sp?id=kb_article&sys_id=KB0000005%20V1.0` to view the article.

The article view page shows a version history section for articles that have been updated. This section includes the version numbers, date updated, and the name of the author or reviser.

-   Click **Latest version** or the version number and current state to expand the version history section.
-   Click the version number to open that particular version of the article.
-   When viewing an outdated article, a message informs the user that a newer updated version is available. The message includes a link to the latest version.

