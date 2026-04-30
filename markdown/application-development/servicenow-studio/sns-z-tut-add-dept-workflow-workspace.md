---
title: Add departmental workflows to your workspace
description: A well-structured workspace improves task visibility, reduces response times, and ensures that fulfillers have all the necessary tools and information in one place. By using Workspaces, departments can standardize processes, reduce manual effort, and improve collaboration—leading to better service delivery, higher productivity, and organization-wide operational improvements.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Tutorial part 3: Expand to a departmental solution, ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Add departmental workflows to your workspace

A well-structured workspace improves task visibility, reduces response times, and ensures that fulfillers have all the necessary tools and information in one place. By using Workspaces, departments can standardize processes, reduce manual effort, and improve collaboration—leading to better service delivery, higher productivity, and organization-wide operational improvements.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  From the Navigator panel, open the **Marketing Services** workspace.

3.  Select the **List** tab.

4.  Select **\(+\) Add list category**.

    ![Under the Marketing Design Request list, select add list category.](../image/sns-z-tut-list-tab.png)

5.  In the **Name** field, enter `Marketing Issues`.

6.  Select **Add**.

7.  Under Marketing Issues, select **\(+\) Add filtered list**.

8.  In the **Name** field, enter `Open`.

9.  In the **Table** field, select **Marketing Issue**.

10. Select **Add**.

11. Under Configurations, select **Apply conditions**.

    ![Apply conditions to your filtered list.](../image/sns-z-tut-apply-conditions.png)

12. Select **\[active\] \[is\] \[true\]** in the condition builder.

13. Select **Apply filter**.

14. Select **Save**.

15. Select **Preview** to open the workspace.

16. Select **Edit**.

17. Select the more options icon \(![](../image/sn-studio-more-options-icon.png)\) for the Critical Tasks data visualization.

18. Select **Delete**.

    ![Delete the Critical Tasks data visualization.](../image/sns-z-tut-delete-data-vis.png)

19. Select **Add new element**.

20. Select **Data visualization**.

21. Select **New Visualization**.

22. Drag the new data visualization to the location where you just deleted Critical tasks from.

23. Resize the data visualization to match the other data visualizations in the row.

    ![Resize the data visualization so it aligns with the other data visualizations.](../image/sns-z-tut-new-data-vis.png)

24. Select **Visualization type** \(Single score\).

25. Select **Pie**.

    ![Create a pie chart visualization for your data.](../image/sns-z-tut-pie-vis.png)

26. Expand the Header and border section.

27. Enter `Open Tasks` in the **Chart title** field.

28. Select **+ Add data source**under **Data sources**.

29. Search for `task`.

30. Select **Task \[task\]**.

31. Select **+ Add custom conditions** in the **Filters** section.

32. Set the conditions to be **\[task\] \[is\] \[Marketing Design Request\] OR \[task\] \[is\] \[Marketing Inquiry\] OR \[task\] \[is\] \[Marketing issue\] AND \[active\] \[is\] \[true\]**.

    ![Apply the conditions for the Task type and Active status.](../image/sns-z-tut-custom-conditions.png)

33. Select **Add this source**.

34. Select **Edit** in the **Group by** section.

35. Set **Field for Task** to **Task type**.

36. Select **Apply**.

    ![Group your pie chart by task type.](../image/sns-z-tut-group-by.png)

37. Resize the Data visualizations using the thumbs in the lower corners.

    ![Resize the data visualizations if you want to.](../image/sns-z-tut-final-data-vis.png)

38. Select **Save** and **Exit editing mode**.


**Parent Topic:**[ServiceNow Studio tutorial part 3: Expand to a departmental solution](../concept/sns-z-tutorial-expand-departmental-solution.md)

