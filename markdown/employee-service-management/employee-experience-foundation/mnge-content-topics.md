---
title: Manage connected content from topic pages
description: Link your desired categories to the topics and track the additions and removals to have easier management of unconnected content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/mnge-content-topics.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Taxonomy and connected content, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Manage connected content from topic pages

Link your desired categories to the topics and track the additions and removals to have easier management of unconnected content.

## Before you begin

Role required: taxonomy\_admin

User criteria required: Taxonomy Manager, Taxonomy Contributor, Topic Manager, Topic Contributor.

## About this task

A Fix script is shipped with the feature that automatically runs when you upgrade. Link your desired categories to the topics manually, for new installations, for new taxonomy created, or for new categories required on the existing taxonomies.

-   The script goes through all the connected content on the topics and identifies the categories for the connected content.
-   The fix script works for all the active taxonomies.
-   The **Catalog and knowledge Categories** tab displays the identified categories to be linked to the topics, after the fix script is successfully executed.
-   Linking a category to a topic bulk-connects all its connected content to the topic.

A weekly scheduled job runs to recognize new content added or removed from the category that can be associated to the topics.

For more information on the execution and modification of the scheduled job, see

-   [Run the scheduled job for content association](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/schduld-job-link-cntnt.md) and [Check for updated content in categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/may-associate-updated-content-categories-topics.md) for manual checking and updation of each record.
-   [Enable connected content autosync system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/may-system-properties-taxonomy-autosync.md) for autosync.

**Important:** The connected content management is available from the Zurich family release.

## Procedure

1.  Navigate to **All** &gt; **Content Taxonomy** &gt; **Topics**.

2.  Go to the **Catalog and knowledge Categories** tab on your desired topic page to add another category, and select **Edit**.

    The following are the available fields on the tab:

    |Field|Value|
    |-----|-----|
    |Content type|Catalog Item, Knowledge Base|
    |Connected Category|Category linked to the topic pages based on the content type|
    |Available content for association|The number of new content items detected on the linked categories|

3.  Select the **Content type** in the pop-up window and select the category to link to the topic page.

    Video describes the process to connect content categories to topic pages 

    All the content in the category is associated with the topic.

4.  You can perform the following content actions:

    1.  Go to **Category** and the related list **Catalog Item** &gt; **New** to add the record.

    2.  Go to **Category** and the related list **Catalog Item** &gt; **Actions on selected rows** &gt; **Delete** to remove the record.

        \[Omitted image "category-delete-content.png"\] Alt text: catalog item removal

5.  [Run the scheduled job for content association](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/schduld-job-link-cntnt.md) to surface the unconnected content of categories.

6.  Select **Save** or **Reload form** the topic page.

    A confirmation message appears on the screen.

    \[Omitted image "pop-up-notification.jpg"\] Alt text: The notification that relevant category has been linked to the topic and content associated to the category is being added to the topic page.

7.  Select **View Details** on the pop-up notification displayed on the topic page to see the content additions and removals available.

8.  Go to **Associated catalog and kb categories** to see the **Update Type**, such as Added or Removed content in the categories.

    \[Omitted image "connected-content-view-add-remove.png"\] Alt text: Associated catalog and kb categories addition and removal updates

9.  Add or dismiss content, as required, with **Update topic with content** or **Dismiss content** respectively.


## Result

Access all the connected content to the categories linked to the topic pages.

## What to do next

Click **Check for updated content in categories** related link to see the content creation source.

\[Omitted image "connected-content-tab.png"\] Alt text: Creation source list of Connected Content tab in a Topic

**Creation source** helps you distinguish and manage the content added from **Category** or by **User**.

-   **[Run the scheduled job for content association](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/schduld-job-link-cntnt.md)**  
Change the scheduled job frequency, as required, to ensure that the notification of new content availability to add to the topic pages is regular and uninterrupted.
-   **[Enable connected content autosync system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/may-system-properties-taxonomy-autosync.md)**  
Content updates are automatically synced when you enable the autosync system property.
-   **[Check for updated content in categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/may-associate-updated-content-categories-topics.md)**  
Track and manage the updated content in categories for better visibility, content maintenance, and performance.

**Parent Topic:**[Taxonomy and connected content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/track-new-content.md)

