---
title: View customizations and compare with current version
description: View the customizations that make up an update set and compare the update to the current version.
locale: en-US
release: xanadu
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Update set use, System update sets, Deploying applications, Building applications]
---

# View customizations and compare with current version

View the customizations that make up an update set and compare the update to the current version.

## Before you begin

Role required: admin

## About this task

The Customer Update **\[sys\_update\_xml\]** table contains one record per customized object.

The customer update record specifies:

-   The update set containing the customized object.
-   The type of action applied to the customized object.
    -   INSERT
    -   INSERT\_OR\_UPDATE
    -   UPDATE
    -   DELETE
-   The type of object customized.
-   The target object of the update.
-   The sys\_id of the customized object \(if it is a change to a particular record\).
-   The user who customized the object.
-   The date and time the object was customized.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Click the update set name.

3.  View the Customer Updates related list.

    You can compare any update to the current version. Right-click the update record and select **Compare to Current**.

    ![Update set with addition of the 'Incident Table' table](../image/UpdateSetRecord.png)


**Related topics**  


[Compare two versions of an article](https://www.servicenow.com/docs/access?context=compare-two-article-versions&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

[Resolve conflicts for an individual record](https://www.servicenow.com/docs/access?context=upgrademon-resolve_conflicts&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

