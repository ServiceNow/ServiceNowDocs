---
title: Create the Marketing department taxonomy
description: Create a marketing department taxonomy on the ServiceNow AI Platform.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tutorial part 3: Expand to a departmental solution, ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Create the Marketing department taxonomy

Create a marketing department taxonomy on the ServiceNow AI Platform.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Advanced Portal Navigation**.

2.  Hover over the **Employee Center** link.

3.  Select the **Preview Employee Center** icon ![](../image/sns-z-tut-preview-emp-center-icon.png).

4.  Select **Open Record**.

5.  Switch the scope to the **Employee Center Pro** application by selecting **here**.

6.  Clear the **Active** check box.

7.  Select **Update** to save your changes.

8.  Select the **Application scope** picker.

9.  Search for **employee**.

    ![Select the application scope picker and search for Employee experience taxonomy.](../image/sns-z-tut-app-scope.png)

10. Select **Employee experience taxonomy**.

11. Navigate to **All** &gt; **Content Taxonomy** &gt; **Taxonomies**.

12. Select the **Employee** taxonomy.

13. Select **New** on the **Child Topics** related list.

14. Enter `Marketing` in the **Name** field.

15. Select and hold \(or right-click\) in the header bar and select **Save**.

    ![Create a new child topic with Marketing as the title.](../image/sns-z-tut-marketing-taxo-record.png)

16. Select the **Marketing** child topic to open it.

17. Select **New**On the **Connected Content** related list.

18. Select **Catalog Item** for the **Content Type**.

19. Select **Marketing Design Request** for the **Catalog Item**.

20. Select **Submit**.

    ![Create a new connected content record for the Marketing design requests.](../image/sns-z-tut-connect-content-1.png)

21. Repeat steps 17-20 for **Marketing Issue**.

    ![Create a new connected content record for the Marketing issues.](../image/sns-z-tut-connect-content-2.png)

22. Repeat steps 17-20 steps for **Marketing Inquiry**.

    ![Create a new connected content record for Marketing inquiries.](../image/sns-z-tut-connect-content-3.png)

23. Select the **Application scope** picker.

24. Search for `marketing`.

25. Select **Marketing Services**.

    ![Search for Marketing Services in the application scope picker.](../image/sns-z-tut-mark-scope.png)

26. Search for `employee` on the platform, in the filter navigator.

27. Select **Employee Center**.

28. Select **Marketing**.


## Result

Observe that the newly created requests are grouped together in the taxonomy under the Marketing topic.

![Newly created issues, inquiries, and requests are grouped together in the taxonomy under the Marketing topic.](../image/sns-z-tut-marketing-final.png)

**Parent Topic:**[ServiceNow Studio tutorial part 3: Expand to a departmental solution](../concept/sns-z-tutorial-expand-departmental-solution.md)

