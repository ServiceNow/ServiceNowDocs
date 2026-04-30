---
title: Taxonomy and connected content
description: Using the taxonomy and content personas, you can keep track and manage the new content updates on the topic pages. Connect new content to the categories linked to the topics. Monitor the categories to track new content available as the associated connected content types.Link your desired categories to the topics and track the additions and removals to have easier management of unconnected content.Change the scheduled job frequency, as required, to ensure that the notification of new content availability to add to the topic pages is regular and uninterrupted.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Content management on topic pages, Manage, Employee Center, Employee Service Management]
---

# Taxonomy and connected content

Using the taxonomy and content personas, you can keep track and manage the new content updates on the topic pages. Connect new content to the categories linked to the topics. Monitor the categories to track new content available as the associated connected content types.

Gain visibility into new and invalid content and manage content life cycle through automation for performance improvement.

You can make the topic pages include the most updated content available for the employees.

-   The taxonomy and topic managers can add, remove, move, and review new content available for the connected content types associated to the categories.
-   You can manually review, add, or dismiss the content updates from the notifications and the **Associated catalog and kb categories** record.
-   Track and manage outdated connected content from a dedicated the **Outdated Connected Content** tab.
-   Alternatively, you can also autosync the new content updates by enabling a **Taxonomy category content autosync** system property.
-   The connected content types supported for the features are Knowledge Base articles and Service Catalog items.

Connected content is available on the Browser Extension for Employee Center. For more information, see [Browser Extension for Employee Center](ecbe-intro.md).

**Parent Topic:**[Content management on topic pages](cm-ec-manage.md)

## Manage connected content from topic pages

Link your desired categories to the topics and track the additions and removals to have easier management of unconnected content.

### Before you begin

Role required: taxonomy\_admin

User criteria required: Taxonomy Manager, Taxonomy Contributor, Topic Manager, Topic Contributor.

### About this task

A Fix script is shipped with the feature that automatically runs when you upgrade to Utah.

Link your desired categories to the topics manually, for new installations, for new taxonomy created, or for new categories required on the existing taxonomies.

**Note:** The feature is only available Utah release onwards.

-   The script goes through all the connected content on the topics and identifies the categories for those connected content.
-   The fix script works for all the active taxonomies.
-   The **Catalog and knowledge Categories** tab displays the identified categories to be linked to the topics, after the fix script is successfully executed.
-   Linking a category to a topic bulk-connects all its connected content to the topic.

A weekly scheduled job runs to recognize new content to be associated to the topics.

For more information on the execution and modification of the scheduled job, see

-   [Run the scheduled job for content association](track-new-content.md#) and  for manual checking and updation of each record.
-    for autosync.

### Procedure

1.  Navigate to **All** &gt; **Content Taxonomy** &gt; **Topics**.

2.  Go to the **Catalog and knowledge Categories** tab on your desired topic page to add another category, and select **Edit**.

    The following are the available fields on the tab:

    |Field|Value|
    |-----|-----|
    |Content type|Catalog Item, Knowledge Base|
    |Connected Category|Category linked to the topic pages based on the content type|
    |Available content for association|The number of new content detected on the linked categories|

3.  Select the **Content type** on the pop-up window and select the category to link to the topic page.

    ![Edit categories to be linked to topics on the pop-up window](../images/content-type-filter-option.jpg "Edit categories window")

    All the content in the category is associated to the topic.

4.  You can perform the following content actions:

    1.  Go to **Category** and the related list **Catalog Item** &gt; **New** to add the record.

    2.  Go to **Category** and the related list **Catalog Item** &gt; **Actions on selected rows** &gt; **Delete** to remove the record.

        ![image.category-delete-content]

5.  [Run the scheduled job for content association](track-new-content.md#) to surface the unconnected content of categories.

6.  Select **Save** or **Reload form** the topic page.

    A confirmation displays on the screen.

    ![The notification that relevant category has been linked to the topic and content associated to the category is being added to the topic page.](../images/pop-up-notification.jpg "Confirmation notifications")

7.  Select **View Details** on the pop-up notification displayed on the topic page to see the content additions and removals available.

8.  View **Associated catalog and kb categories** to see the **update type**, such as Added or Removed.

9.  Add or dismiss content, as required, with **Update topic with content** or **Dismiss content** respectively.


### Result

Access all the connected content to the categories linked to the topic pages.

### What to do next

Click the **Add/remove content from categories** related link to see the **update type**, such as Added or Removed.

![image.connected-content-view-add-remove]

## Run the scheduled job for content association

Change the scheduled job frequency, as required, to ensure that the notification of new content availability to add to the topic pages is regular and uninterrupted.

### Before you begin

Role required: admin

### About this task

**Surface New Unconnected Content of Categories** helps you identify the new unconnected content.

-   Use the scheduled job for manual additions and removals of content.
-    for automatic additions and removals of content.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** &gt; **Surface New Unconnected Content of Categories**.

2.  Select your preferred **Run** time option, for the scheduled job, from the available list on the field.

    ![This field, Run, lists out frequency options for the scheduled job to execute periodically.](../images/schdled-job-runtime.png "Scheduled job run-time options")

    **Note:** The default scheduled job run-time is weekly. Edit and update the frequency of execution, as required.

3.  Select **View Details** on the pop-up notification displayed on the topic page to see the new content available for association.

    ![The notification states new content is available for association with a link for view details.](../images/new-content-available.jpg "New content availability notification")

4.  View **Associated catalog and kb categories** to see the **update type**, such as Added or Removed.

    ![image.connected-content-view-add-remove]

5.  Add or dismiss content, as required, with **Update topic with content** or **Dismiss content** respectively.


